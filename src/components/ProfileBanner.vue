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
   padding-top: 30px;
   padding-left: 70px;
   font-size: 22px;
}
</style>