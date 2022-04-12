<template>
  <footer class="footer">
    <div class="container">
      <ul class="navbar-list">
        <li class="navbar-item">
          <router-link class="navbar-link" :to="{name: 'Home'}">Home</router-link>
        </li>
        <li class="navbar-item">
          <router-link class="navbar-link" :to="{name: 'About' }">About</router-link>
        </li>
      </ul>
    </div>
  </footer>
</template>
