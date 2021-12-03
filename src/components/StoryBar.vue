<template>
  <div class="story-bar">
    <Avatar :size="41" /> <Avatar :size="41" /> <Avatar :size="41" />
    <Avatar :size="41" /> <Avatar :size="41" /> <Avatar :size="41" /> <Avatar :size="41" />

  </div>
</template>

<script>
import Avatar from '@/components/Avatar'

export default {
  name: 'StoryBar',
  components: {
    Avatar
  }
}
</script>

<style scoped>
.story-bar {
  height: 60px;
  align-items: center;
  border-block: rgba(255, 255, 255, 0.925);
  display: inline-block;
}
avatar {
  padding-left: 8px;
}
</style>