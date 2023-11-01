<style lang="scss">
@import '@/scss/app';
</style>

<script setup lang="ts">
import MainLayout from '@/components/layouts/MainLayout.vue'
import { RouterView } from 'vue-router'
</script>

<template>
  <main-layout> <router-view /> </main-layout>
</template>
