<template>
  <div class="color-black posts-holder">
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
    <div>here</div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import type { Post } from '@/interfaces/Posts.ts'

export default defineComponent({
  data() {
    return {
      posts: [] as Post[]
    }
  },
  mounted() {
    fetch('https://api.escuelajs.co/api/v1/products')
      .then((resp) => resp.json())
      .then((respData: Post[]) => {
        this.posts = respData
      })
  }
})
</script>

<style scoped>
.posts-holder {
  padding-top: 50px;
}
</style>
