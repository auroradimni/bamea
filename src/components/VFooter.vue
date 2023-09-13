<template>
  <footer class="footer">
    <div class="social-media pad-xxl-b">
      <MDBBtn tag="a" color="primary" href="#!" floating size="lg">
        <MDBIcon iconStyle="fab" icon="instagram"></MDBIcon>
      </MDBBtn>
      <MDBBtn tag="a" color="primary" href="#!" floating size="lg">
        <MDBIcon iconStyle="fab" icon="linkedin-in"></MDBIcon>
      </MDBBtn>
      <MDBBtn tag="a" color="primary" href="#!" floating size="lg">
        <MDBIcon iconStyle="fab" icon="twitter"></MDBIcon>
      </MDBBtn>
    </div>
    <div class="rounder-holder">
      <div class="rounded-corner"></div>

      <div class="rounded-corner-right"></div>
    </div>
  </footer>
</template>

<script lang="ts">
import { MDBBtn, MDBIcon } from 'mdb-vue-ui-kit'
export default {
  name: 'VFooter',
  components: {
    MDBBtn,
    MDBIcon
  },
  data() {
    return {}
  }
}
</script>

<style lang="scss" scoped>
.footer {
  position: fixed;
  bottom: 0;
  right: 0;
  left: 0;
  .social-media {
    position: relative;
    z-index: 1;
    display: flex;
    justify-content: center;
    gap: 20px;
  }
  .rounder-holder {
    .rounded-corner {
      &::after {
        content: '';
        padding: 50%;
        background-color: mapget($colors, 'black');
        border-top-right-radius: 100%;
      }
      position: absolute;
      left: 0;
      right: 70%;
    }
    .rounded-corner-right {
      &::after {
        content: '';
        padding: 50%;
        background-color: mapget($colors, 'coral-blue');
        border-top-left-radius: 100%;
      }
      position: absolute;
      left: 62%;
      right: 0;
    }
  }
}
</style>
