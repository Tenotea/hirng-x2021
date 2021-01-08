<template>
  <div class="nav animate__animated animate__flipInX">
    <ul class="nav__container">
      <router-link v-for="option in navOptions" :key="option.id"  :to="option.route">
        <li class="nav__container--item">
          {{ option.name }}
        </li>
      </router-link>
    </ul>
    <div class="nav__avatar">
      <div class="avatar"></div>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      navOptions: [
        {
          id: 1,
          name: 'home',
          route: '/'
        },
        {
          id: 2,
          name: 'about',
          route: '/'
        },
        {
          id: 3,
          name: 'gallery',
          route: '/'
        },
        {
          id: 4,
          name: 'contact',
          route: '/'
        }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
  .nav {
    width: 100%;
    margin-top: 60px;
    position: relative;
    &__container {
      display: flex;
      max-width: 1000px;
      list-style: none;
      margin: auto;
      align-items: center;
      justify-content: space-between;
      &--item {
        text-transform: uppercase;
        font-size: 1.2em;
        font-weight: lighter;
        color: rgb(255, 255, 255);
        transition: 200ms ease-out transform;
        &:hover {
          transform: translateY(-6px);
          transition: 200ms ease-in transform;
        }
      }
    }
    &__avatar {
      position: absolute;
      pointer-events: none;
      top: 50%;
      left: 50%;
      background: transparent;
      width: 100%;
      transform: translate(-50%, -50%);
      .avatar {
        $size: 70px;
        width: $size;
        height: $size;
        border: 2px solid rgba(202, 202, 202, 0.308);
        margin: auto;
        border-radius: 50%;
        background: url('../assets/p.png');
        background-position: top center;
        background-repeat: no-repeat;
        background-size: cover;
      }
    }
  }
</style>