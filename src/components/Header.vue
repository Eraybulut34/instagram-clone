<template>
  <header class="header">
    <Container class="header-inner">
      <router-link to="/" class="logo"> Instagram </router-link>
      <form class="search">
        <input type="text" placeholder="Search" class="search" />
      </form>
      <nav class="navigation">
        <router-link to="/">
          <IconHomeFill v-if="$route.name === 'Home'" />
          <IconHome v-else />
        </router-link>
        <router-link to="/direct">
          <IconDirectFill v-if="$route.name === 'Direct'" />
          <IconDirect v-else />
        </router-link>
        <router-link to="/explore">
          <IconExploreFill v-if="$route.name === 'Explore'" />
          <IconExplore v-else
        /></router-link>
        <router-link to="/profile"><Avatar :size="29"/></router-link>
      </nav>
    </Container>
  </header>
</template>

<script>
import IconHome from '@/icons/home.svg'
import IconHomeFill from '@/icons/home-fill.svg'
import IconDirect from '@/icons/direct.svg'
import IconDirectFill from '@/icons/direct-fill.svg'
import IconExplore from '@/icons/explore.svg'
import IconExploreFill from '@/icons/explore-fill.svg'
import Container from '@/components/Container'
import Avatar from '@/components/Avatar'

export default {
  name: 'MainHeader',
  components: {
    IconHome,
    IconHomeFill,
    Container,
    IconDirect,
    IconDirectFill,
    IconExplore,
    IconExploreFill,
    Avatar
  }
}
</script>

<style scoped>
.header {
  border-bottom: 1px solid rgb(var(--b6a));
  position: fixed;
  left: 0;
  right: 0;
  top: 0;
  border-bottom: 1px solid rgb(var(--b6a));
  background-color: white;
}
.header-inner {
height: var(--header-height);
  display: flex;
  align-items: center;
  justify-content: center;
  @media (--t) {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    align-items: center;
    height: 60px;
  }
}
.logo {
  font-size: 1.6rem;
  font-weight: bold;
}
.search {
  display: none;
  @media (--t) {
    display: block;
    text-align: center;

    input {
      border: 1px solid rgb(var(--b6a));
      border-radius: 4px;
      background-color: rgb(var(--b3f));
      padding-left: 20px;
      padding-right: 20px;
    }
  }
}

.navigation {
  z-index: 90;
  position: fixed;
  left: 0;
  right: 0;
  bottom: 0;
  background-color: white;
  border-top: 1px solid rgb(var(--b6a));
  height: 5rem;
  display: flex;
  align-items: center;
  justify-content: space-around;
  @media (--t) {
    height: auto;
    border: 0;
    position: static;
    justify-content: flex-end;
    a {
      margin-left: 1.3rem;
    }
  }
}
</style>
