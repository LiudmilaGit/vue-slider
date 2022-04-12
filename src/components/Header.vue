<template>
  <header class="navbar">
    <div class="container">
      <div class="navbar-content">
        <a href="/" class="navbar-logo">Logo</a>
        <ul class="navbar-list">
          <li class="navbar-item">
            <router-link class="navbar-link" :to="{name: 'Home'}">Home</router-link>
          </li>
          <li class="navbar-item">
            <router-link class="navbar-link" :to="{name: 'About' }">About</router-link>
          </li>
        </ul>
      </div>
    </div>
  </header>
</template>
