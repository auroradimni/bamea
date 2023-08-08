<template>
  <header>
    <div class="header" id="header">
      <RouterLink :to="{ name: 'home' }">Home</RouterLink>
      <RouterLink :to="{ name: 'posts' }"> Posts</RouterLink>
      <RouterLink :to="{ name: 'about' }">About us</RouterLink>
      <RouterLink :to="{ name: 'contact' }">Contact us</RouterLink>

      <div>
        <div class="logo">
          <h1>Bamea</h1>
        </div>
        <p class="moto">good thing take time</p>
      </div>
    </div>
  </header>
  <RouterView />
</template>

<script lang="ts">
import { RouterLink, RouterView } from 'vue-router'
export default {
  name: 'VHeader',
  components: {
    RouterView,
    RouterLink
  },
  data() {
    return {}
  }
}
</script>

<style scoped lang="scss">
header {
  div {
    &.header {
      & a {
        color: mapget($colors, 'primary');
      }
      display: flex;
      justify-content: right;
      gap: 50px;
      position: fixed;
      top: 30px;
      max-height: 50px;
      left: 0;
      right: 0;
      text-size-adjust: 30px;
      color: mapget($colors, 'primary');
      padding: 20px;
    }
  }

  div {
    &.logo {
      position: fixed;
      font-family: 'Segoe Script';
      font-weight: bold;
      font-style: normal;
      text-align: left;
      letter-spacing: 1px;
      color: #1c7e98;
      top: 0;
      left: 0;
      margin-left: 0.5%;
    }
  }
}
.moto {
  position: fixed;
  font-family: 'Papyrus';
  font-weight: bold;
  font-style: bold;
  text-align: left;
  color: #101108;
  top: 5%;
  left: 0;
  margin-left: 0.5%;
}
</style>
