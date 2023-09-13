<template>
  <div class="color-black posts-holder">
    <div v-if="posts.length === 0" class="grid">
      <div v-for="i in 35" class="flex skeleton" :key="i">
        <div class="thin skeleton_loader dark thin w-100"></div>
      </div>
      <div>{{ fullname }}</div>

      <input id="name" name="name" v-model="name" />
      <input id="surname" name="surname" v-model="surname" />
    </div>
    <div class="grid" v-else>
      <div v-for="post in posts" :key="post.id" class="flex">
        {{ post.title }}
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import type { Post } from '@/interfaces/Posts.ts'

export default defineComponent({
  data() {
    return {
      posts: [] as Post[],
      name: 'Aurora' as string,
      surname: 'Dimni' as string
    }
  },
  computed: {
    fullname: {
      get(): string {
        return this.name + ' ' + this.surname
      },
      // setter
      set(newValue: string): void {
        ;[this.name, this.surname] = newValue.split(' ')
      }
    }
  },

  beforeCreate() {
    console.log('beforeCreate')
  },
  created() {
    console.log('created')
  },
  beforeMount() {
    console.log('beforeMount')
  },
  mounted() {
    console.log('mounted')

    fetch('https://api.escuelajs.co/api/v1/products')
      .then((resp) => resp.json())
      .then((respData: Post[]) => {
        setTimeout(() => {
          this.posts = respData
        }, 5000)
      })
  },
  beforeUpdate() {
    console.log('beforeUpate')
  },
  updated() {
    console.log('updated')
  },
  beforeUnmount() {
    console.log('beforeUnmount')
  },
  unmounted() {
    console.log('unmounted')
  }
})
</script>

<style scoped>
.posts-holder {
  padding-top: 50px;
  .grid {
    gap: 20px;
    .flex {
      display: flex;
      justify-content: center;
    }
    display: grid;
    grid-template-columns: repeat(4, 1fr);
  }
}
</style>
