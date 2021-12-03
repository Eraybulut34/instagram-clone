<template>
  <figure class="avatar">
    <img :src="src" :alt="alt" :width="size" :height="size" />
    <slot />
  </figure>
</template>

<script>
export default {
  name: 'Avatar',
  props: {
    src: {
      type: String,
      default:
        'https://ru-static.z-dn.net/files/d8e/7c98f3e5129a4ec4c0f0f3113de228b7.png'
    },
    alt: {
      type: String
    },
    size: {
      type: Number
    }
  }
}
</script>

<style scoped>
.avatar {
    border: 3px solid black;

    border-radius: 999px;
    display: inline-flex;
     background: linear-gradient(
    219deg,
    rgba(184, 63, 140, 1) 0%,
    rgba(237, 158, 90, 1) 100%
  );


}
  img {
    border-radius: inherit;
    border: 2px solid white;
  }
</style>