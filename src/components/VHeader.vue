<template>
  <div class="header d-flex pad-lg-r pad-lg-l bg-color-white pad-xxl-t pad-xs-b" id="header">
    <div class="logo-holder">
      <div class="logo color-light-blue font-size-lg">Bamea</div>
      <p class="moto font-size-xs">good thing take time</p>
    </div>
    <div class="desktop-nav">
      <div class="routers d-flex gap-xs">
        <RouterLink :to="{ name: 'home' }">Home</RouterLink>
        <RouterLink :to="{ name: 'posts' }"> Posts</RouterLink>
        <RouterLink :to="{ name: 'about' }">About us</RouterLink>
        <div class="search-bar">
          <input
            ref="input"
            class="input"
            type="text"
            v-model="search"
            placeholder="Search..."
            @input="filterItems"
          />
          <font-awesome-icon
            class="font-awsome cursor-pointer"
            :icon="['fas', 'magnifying-glass']"
          />
        </div>
      </div>
    </div>
    <font-awesome-icon
      :icon="['fas', 'bars']"
      class="mobile-nav cursor-pointer color-primary"
      @click="openNav"
    />
    <div class="mobile-nav holder" ref="mobile">
      <span class="cursor-pointer close color-black" @click="closeNav">X</span>
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
    return {
      search: '' as string
    }
  },
  methods: {
    filterItems() {
      console.log(this.search)
    },
    openNav() {
      ;(this.$refs.mobile as HTMLDivElement).classList.add('show')
    },
    closeNav() {
      ;(this.$refs.mobile as HTMLDivElement).classList.remove('show')
    }
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
    align-items: center;
    max-width: 500px;
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
      color: mapget($colors, 'black');
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
  .mobile-nav {
    display: none;
    z-index: 2;
    &.holder {
      max-width: 250px;
      margin-right: -250px;
      width: 100%;
      background-color: mapget($colors, 'white');
      box-shadow: 10px 10px 10px 10px;
      position: fixed;
      right: 0;
      top: 0;
      bottom: 0;
      transition: margin 700ms;

      .close {
        position: absolute;
        display: flex;
        align-items: center;
        justify-content: center;
        right: 10px;
        top: 10px;
        width: 30px;
        height: 30px;
      }
    }
    &.show {
      margin-right: 0;
      transition: margin 700ms;
    }
  }
}

@media screen and (max-width: breakpointValue(sm)) {
  .desktop-nav {
    display: none;
  }
  .header {
    .mobile-nav {
      display: flex;
    }
  }
}
</style>
