<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <div class="about">
    <h3 class="title color-primary">About us</h3>
    <div class="paragraph">
      <p>
        Hello everyone, in this blog we want to share our thoughts and experiences with you, the
        topics we will mostly talk about are: technology, lifestyle, books, social media, etc.We
        hope you enjoy your free time reading our articles.
      </p>
      <div>
        <h2 class="logo1 color-primary" style="font-family: Segoe Script">Bamea</h2>
        <p class="moto1 color-black" style="font-family: Papyrus">good things take time</p>
      </div>
    </div>
  </div>
</template>

<style scoped lang="scss">
.about {
  box-shadow: 0 5px 10px 0 #1f95a2;
  max-width: 600px;
  margin: auto;
  text-align: center;
  height: 400px;
  right: 0%;
  left: 0%;
  padding: 50px;
  position: fixed;
  top: 100px;

  .title {
    text-align: center;
    font-style: normal;
    font-family: 'Segoe Script';
  }
  div {
    &.logo1 {
      position: fixed;
      font-family: 'Segoe Script';
      font-weight: bold;
      font-style: normal;
      text-align: center;
    }
    &.moto1 {
      position: fixed;
      font-family: 'Papyrus';
      font-weight: bold;
      font-style: bold;
      text-align: left;
    }
  }
}
.paragraph {
  color: black;
}
</style>
