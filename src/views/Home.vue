<template>
  <div class="home">
    <username :name="currentProfile.name" />
    <profile-image />
    <bottom-navigation />
    <social-media :social-media="currentProfile.social_media" />
  </div>
</template>

<script>
import Username from '@/components/Username'
import ProfileImage from '@/components/ProfileImage'
import BottomNavigation from '@/components/BottomNavigation'
import SocialMedia from '@/components/SocialMedia'
import Axios from 'axios'
export default {
  name: 'Home',
  components: {
    Username,
    ProfileImage,
    BottomNavigation,
    SocialMedia,
  },

  data () {
    return {
      currentProfile: {}
    }
  },

  async created () {
    try {
      const APIResponse = (await Axios.get('https://hirng-x2021.glitch.me/api')).data
      this.currentProfile = APIResponse
    } catch (e) {
      // Handle error
    }

  }
}

</script>

<style lang="scss">
  .home {
    width: 100%;
    min-height: 100vh;
    overflow-x: hidden;
    // padding-bottom: 30px;
    background: linear-gradient(to right, #bd0f4d 50%, #cb2964 50%);
  }
</style>
