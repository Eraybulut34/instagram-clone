<template>
<div class="profile-banner">
<Avatar :size="140"/><div class="username"> 
<CustomText >eraybulut34</CustomText></div>
</div>
</template>

<script>
import Avatar from '@/components/Avatar'
import CustomText from '@/components/CustomText'

export default {
  name: 'ProfileBanner',
  components: {
      Avatar,
      CustomText
  }

}
</script>

<style scoped>
.profile-banner{
  display: flex;
}
.username{
   padding-top: 1.9rem;
   padding-left: 4.5rem;
   font-size: 1.4rem;
}
</style>
