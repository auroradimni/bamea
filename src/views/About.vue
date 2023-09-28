<template>
  <div class="d-flex w-100 gap-lg holder">
    <div
      ref="img"
      class="about-img flex-grow d-flex justify-content-center align-items-center w-100"
    >
      <div class="logo-holder d-grid">
        <div class="logo font-size-xl color-primary">Bamea</div>
        <div class="moto font-size-md color-black">good things take time</div>
      </div>
      <img class="img w-100 h-100" src="@/assets/BAMEA.png" />
    </div>
    <div
      ref="txt"
      class="about-text flex-grow w-100 d-flex justify-content-center align-items-center"
    >
      <p>
        Welcome to Bamea, your source for tech,lifestyle,and more.Our team of experts shares
        insights to empower and inspire you. Stay informed, entertained, and connected with our
        engaging articles. Join us on this journey of discovery!
      </p>
    </div>
  </div>
</template>

<script lang="ts">
export default {
  data() {
    return {}
  },
  mounted() {
    setTimeout(() => {
      ;(this.$refs.txt as HTMLDivElement).classList.add('m-0')
      ;(this.$refs.img as HTMLDivElement).classList.add('m-0')
    })
  }
}
</script>

<style lang="scss" scoped>
.holder {
  @media screen and (max-width: breakpointValue(sm)) {
    flex-direction: column;
    align-items: end;
  }
  .logo-holder {
    position: absolute;
    text-align: center;
    z-index: 2;
    font-style: bold;

    .logo {
      font-family: 'Segoe Script';
    }
    .moto {
      font-family: 'Papyrus';
      font-style: bold;
    }
  }
  .about-img {
    margin-top: -500px;
    .img {
      max-width: 400px;
      aspect-ratio: 3.5/3;
    }
    &.m-0 {
      transition: margin 700ms;
      margin: 0;
    }
  }

  .about-text {
    margin-bottom: -1500px;

    &.m-0 {
      transition: margin 700ms;
      margin: 0;
    }
  }
}
</style>
