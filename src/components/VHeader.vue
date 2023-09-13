<template>
  <div class="header d-flex pad-xl-r pad-xl-l bg-color-white pad-xl-t pad-xs-b" id="header">
    <div class="logo-holder">
      <div class="logo color-light-blue font-size-lg">Bamea</div>
      <p class="moto font-size-xs">good thing take time</p>
    </div>
    <div class="routers d-flex gap-xs">
      <RouterLink :to="{ name: 'home' }">Home</RouterLink>
      <RouterLink :to="{ name: 'posts' }"> Posts</RouterLink>
      <RouterLink :to="{ name: 'about' }">About us</RouterLink>
    </div>
    <div class="image-holder">
      <img class="image-top" src="@/assets/top.svg" />
    </div>
  </div>
</template>

<script lang="ts">
import { RouterLink } from 'vue-router'
export default {
  name: 'VHeader',
  components: {
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
  align-items: center;
  justify-content: space-between;
  box-sizing: border-box;

  .routers {
    flex-grow: 1;
    justify-content: space-between;
    max-width: 500px;
    & a {
      color: mapget($colors, 'primary');
      z-index: 20;
      justify-content: space-between;
    }
  }

  position: fixed;
  top: 0px;
  max-height: 100px;
  left: 0;
  right: 0;
  text-size-adjust: 30px;
  color: mapget($colors, 'primary');

  .logo-holder {
    flex-grow: 1;
    .logo {
      line-height: 22px;
      font-family: 'Segoe Script';
      font-weight: bold;
      font-style: normal;
      text-align: left;
      top: 0;
      margin-left: 0.3%;
    }
    & .moto {
      font-family: 'Papyrus';
      font-weight: bold;
      font-style: bold;
      text-align: left;
      color: #101108;
    }
  }

  .image-holder {
    height: 100%;
    width: 100%;
    position: fixed;
    top: -1px;
    right: -1px;
    max-width: 300px;
    max-height: 50px;
    .image-top {
      width: 100%;
      height: 100%;
    }
  }
}
</style>
