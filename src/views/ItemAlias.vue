<template>
  <div>
    <div class="wrapper-person">
      <div v-if="item">
        <img :src="item.img" :alt="item.description" />
        <h1 class="title color">{{ item.title }}</h1>
        <p>{{ item.description }}</p>
        <AppItem :info="item.info" />
        <div class="position">
          <router-link class="btn btnPrimary" to="/">
            Back to Home
          </router-link>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import items from '@/seeders/items'
import AppItem from '@/components/UI/AppItem.vue'
export default {
  components: { AppItem },
  data() {
    return {
      items: items,
      item: null
    }
  },
  created() {
    const alias = this.$route.params.itemAlias
    const item = items.find(el => el.alias === alias)
    this.item = item
  }
}
</script>

<style lang="scss" scoped>
.wrapper-person {
  text-align: center;
}
.color {
  color: white;
}

.card-stats {
  border-radius: 14px;
  margin: 20px 0;
}
</style>
