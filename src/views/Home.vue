<template>
  <carousel :settings="settings" :breakpoints="breakpoints">
    <slide class="card__wrapper" v-for="item in items" :key="item.id">
      <card
        :name="`${item.lvl}`"
        :title="item.title"
        :imgUrl="item.img"
        :link="'/' + item.alias">
        <template #body>
          {{ item.description }}
        </template>
        <template #footer>
          <AppItem :info="item.info" />
        </template>
      </card>
    </slide>
    <template #addons>
      <Navigation />
    </template>
  </carousel>
</template>

<script>
import Items from '@/seeders/items.js'
import Card from '@/components/UI/Card.vue'
import 'vue3-carousel/dist/carousel.css'
import { Carousel, Slide, Navigation } from 'vue3-carousel'
import AppItem from '@/components/UI/AppItem.vue'

export default {
  data() {
    return {
      items: Items,
      settings: {
        itemsToShow: 2,
        wrapAround: true,
        snapAlign: 'center'
      },
      breakpoints: {
        300: {
          itemsToShow: 1
        },
        700: {
          itemsToShow: 2
        }
      }
    }
  },

  components: {
    Card,
    Carousel,
    Slide,
    Navigation,
    AppItem
  }
}
</script>
