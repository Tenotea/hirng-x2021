<template>
  <div class="image">
    <div class="image__container">
      <img src="../assets/p.png" alt="a_certain_image" class="image__container--content">
    </div>
  </div>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
  .image{
    &__container {
      max-width: 800px;
      height: 700px;
      background: #cb2964;
      margin: 40px auto;
      box-shadow: -6px 8px 20px rgba(#000000, 0.3);
      &--content {
        display: block;
        margin: auto;
        width: auto;
        height: 100%;
      }
    }
  }
</style>
