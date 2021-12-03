<template>
  <div class="home">
   

    <div class="timeline">
          <div class="story-bar">
       <StoryBar/>
    </div>
      <Post /><Post /><Post /><Post /><Post />
    </div>
    <div class="sidebar">
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Cupiditate
      tempore, minima eligendi minus animi voluptate, incidunt exercitationem
      inventore facilis eos rem nisi dicta possimus alias obcaecati explicabo
      adipisci unde corrupti!
    </div>
  </div>
</template>

<script>
import Post from '@/components/Post.vue'
import StoryBar from '@/components/StoryBar.vue'

export default {
  name: 'Home',
  components: {
    Post,
    StoryBar

  }
}
</script>

<style scoped>
.home {
  min-width: 605px;
  margin-left: auto;
  margin-right: auto;

  @media (--t) {
    min-width: none;
    display: grid;
    grid-template-columns: 1fr 295px;
    grid-gap: 30px;
  }
}
.sidebar {
  display: none;
  @media (--t) {
    display: block;
  }
}
</style>
