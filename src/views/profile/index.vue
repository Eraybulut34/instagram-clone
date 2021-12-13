<template>
  <div class="home">
<ProfileBanner/> <br>
<div class="nav">
  <router-link to="/profile">Post</router-link>
   <router-link to="/profile/igtv">IGTV</router-link>
    <router-link to="/profile/save">Save</router-link>
     <router-link to="/profile/tag">Tag</router-link>
</div>

   <router-view/>

  </div>
</template>

<script>
import ProfileBanner from '@/components/ProfileBanner'

export default {
  name: 'Profile',
  components: {
    ProfileBanner

  }
}
</script>

<style scoped>
.home{
   min-width: 38rem;
  margin-left: auto;
  margin-right: auto;

  @media (--t) {
    min-width: none;
    display: grid;
    grid-template-columns: 1fr 18.5rem;
    grid-gap: 30px;
  }
}
.nav{
  align-items: center;
  justify-content: center;
}


</style>
