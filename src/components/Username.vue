<template>
  <div class="username">
    <h1 class="username__content animate__animated animate__fadeInDown"> {{ name }} </h1>
  </div>
</template>

<script>
export default {
  props: {
    name: {
      type: String,
      default: 'LOADING...'
    }
  }
}
</script>

<style lang="scss" scoped>
  .username {
    padding-top: 1.5em;
    &__content {
      font-weight: lighter;
      letter-spacing: 1em;
      font-size: 1.8em;
      text-align: center;
      color: white;
    }
  }
</style>