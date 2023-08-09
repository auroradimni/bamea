<template>
  <div class="header d-flex pad-xl-r pad-xl-l bg-color-white" id="header">
    <div class="logo-holder">
      <div class="logo">
        <h1>Bamea</h1>
      </div>
      <p class="moto">good thing take time</p>
    </div>
    <div class="routers d-flex gap-md">
      <RouterLink :to="{ name: 'home' }">Home</RouterLink>
      <RouterLink :to="{ name: 'posts' }"> Posts</RouterLink>
      <RouterLink :to="{ name: 'about' }">About us</RouterLink>
      <RouterLink :to="{ name: 'contact' }">Contact us</RouterLink>
    </div>
    <div class="top-corner"></div>
  </div>
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
.header {
  z-index: 10;
  box-shadow: 0px 3px 10px 0px #707070;

  .routers {
    & a {
      color: mapget($colors, 'primary');
    }
  }
  justify-content: space-between;
  gap: 50px;
  position: fixed;
  top: 0px;
  max-height: 150px;
  left: 0;
  right: 0;
  text-size-adjust: 30px;
  color: mapget($colors, 'primary');

  .logo-holder {
    .logo {
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
    .moto {
      font-family: 'Papyrus';
      font-weight: bold;
      font-style: bold;
      text-align: left;
      color: #101108;
      top: 5%;
      left: 0;
      margin-left: 0.5%;
    }
  }
  div.top-corner {
    position: fixed;
    width: 1398px;
    height: 400px;

    border-color: #707070;
    border-width: 1px;
    border-style: solid;

    background: #ada936;
    top: -350px;
    left: 500px;
    right: 0%;
    border-radius: 100%;
    opacity: 1;
  }
}
</style>
