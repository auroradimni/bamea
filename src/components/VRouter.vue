<template>
  <div class="routers d-flex gap-xs">
    <div v-bind="$attrs" class="d-flex gap-xs justify-content-around w-100">
      <RouterLink :to="{ name: 'home' }">Home</RouterLink>
      <RouterLink :to="{ name: 'posts' }"> Posts</RouterLink>
      <RouterLink :to="{ name: 'about' }">About us</RouterLink>
    </div>

    <div class="search-bar">
      <input
        ref="input"
        class="input"
        type="text"
        v-model="search"
        placeholder="Search..."
        @input="filterItems"
      />
      <font-awesome-icon class="font-awsome cursor-pointer" :icon="['fas', 'magnifying-glass']" />
    </div>
  </div>
</template>

<script lang="ts">
import { RouterLink } from 'vue-router'

export default {
  components: {
    RouterLink
  },
  data() {
    return {
      search: '' as string
    }
  },
  methods: {
    filterItems() {
      console.log(this.search)
    }
  }
}
</script>

<style lang="scss" scoped>
.routers {
  display: flex;
  flex-grow: 1;
  justify-content: space-between;
  align-items: center;
  max-width: 500px;
  .router-link-active {
    border-bottom: 2px solid mapget($colors, 'secondary');
    color: mapget($colors, 'lightGray');
  }

  & .router-holder {
    flex-direction: column;
  }
  & a {
    color: mapget($colors, 'primary');
    z-index: 20;
    justify-content: space-between;
  }
  .search-bar {
    display: flex;
    align-items: center;
    border: mapget($colors, 'primary') solid 1px;
    border-radius: 15px;
    .font-awsome {
      padding-right: 15px;
    }
    .input {
      border: none;
      padding-left: 10px;
      border-radius: 15px;
      max-width: 170px;
      &:focus {
        outline: none;
      }
    }
  }
}
</style>
