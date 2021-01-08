<template>
  <div class="social animate__animated animate__slideInRight">
    <div class="social__container">
      <a :href="`https://instagram.com/${links && links.instagram}`" target="_blank">
        <img src="../assets/instagram.png" alt="" class="social__container--icons">
      </a>
      <a :href="`https://twitter.com/${links && links.twitter}`" target="_blank">
        <img src="../assets/twitter.png" alt="" class="social__container--icons">
      </a>
      <a :href="`https://snapchat.com/add/${links && links.snapchat}`" target="_blank">
        <img src="../assets/snapchat.png" alt="" class="social__container--icons">
      </a>
      <a :href="`mailto:${links && links.email}`" target="_blank">
        <img src="../assets/email.png" alt="" class="social__container--icons">
      </a>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    socialMedia: {
      type: Object,
      default: () => {}
    }
  },

  computed: {
    links () {
      return this.socialMedia
    }
  }
}
</script>

<style scoped lang="scss">
  .social {
    position: fixed;
    background: transparent;
    pointer-events: none;
    top: 0;
    right: 0;
    height: 100vh;
    display: flex;
    flex-direction: column;
    padding: 0px 30px 0px 6px;
    &__container {
      display: flex;
      flex-direction: column;
      margin: auto;
      &--icons {
        width: 35px;
        height: auto;
        display: block;
        margin: 10px 0px;
        pointer-events: all;
      }
    }
  }
</style>
