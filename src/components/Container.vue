<template>
<div class="container">
<slot/>
</div>
</template>

<script>
export default {
  name: 'Container',

}
</script>

<style scoped>
.container{
  max-width: 59rem;
  margin-left: auto;
  margin-right: auto;
  margin-top: 0rem;
}

</style>
