<style lang="scss">
@import '@/scss/app';

div.rounded-corner {
  position: fixed;
  bottom: -20px;
  left: -20px;
  width: 200px;
  height: 30vh;
  background-color: #000000;
  border-top-right-radius: 300px;
  overflow: hidden;
}
div.rounded-cornerright {
  position: fixed;
  bottom: -70px;
  right: -80px;
  width: 350px;
  height: 60vh;
  background-color: #065267;
  border-top-left-radius: 400px;
  overflow: hidden;
  border-color: #707070;
  border-width: 1px;
  border-style: solid;
  color: #0a6e89;
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
</style>

<script setup lang="ts">
import Header from '@/components/Header.vue'
</script>

<template>
  <Header />
  <div class="rounded-corner"></div>
  <div class="rounded-cornerright"></div>
  <div class="top-corner"></div>
</template>
