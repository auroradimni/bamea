<template>
  <div class="main-layout pad-xxl-r pad-xxl-l">
    <VHeader />
    <div class="content">
      <slot> </slot>
    </div>
    <VFooter />
  </div>
</template>

<script lang="ts">
import VHeader from '@/components/VHeader.vue'
import VFooter from '@/components/VFooter.vue'

export default {
  components: {
    VHeader,
    VFooter
  },
  data() {
    return {}
  }
}
</script>

<style lang="scss" scoped>
.main-layout {
  min-height: 100vh;
  width: 100%;
  overflow-x: hidden;
  overflow-y: auto;
  box-sizing: border-box;
  .content {
    margin-top: 130px;
  }
}
</style>
