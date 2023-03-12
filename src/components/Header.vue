<template>
  <header>
    <div class="header" id="header">
      <div>Search</div>
      <RouterLink :to="{ name: 'home' }">Home</RouterLink>
      <RouterLink :to="{ name: 'about' }">About us</RouterLink>
      <RouterLink :to="{ name: 'contact' }">Contact us</RouterLink>
      <div class="logo">
        <img src="../assets/download.webp" alt="logo" />
      </div>
    </div>

    <RouterView />
  </header>
</template>

<script>
import { RouterLink, RouterView } from 'vue-router'
export default {
  name: 'Header',
  components: {
    RouterView,
    RouterLink
  },
  data() {
    return {}
  }
}
</script>

<style scoped>
div.header {
  display: flex;
  justify-content: right;
  gap: 50px;
  position: fixed;
  top: 0;
  max-height: 50px;
  background: transparent;
  left: 0;
  right: 0;
  text-size-adjust: 30px;
  color: rgb(24, 120, 120);
  padding: 20px;
}
div.logo {
  height: 50px;
  top: 5;
  left: 0;
  justify-content: left;
  position: absolute;
  display: flex;
  padding: -50px;
  margin-left: 20px;
}
</style>
