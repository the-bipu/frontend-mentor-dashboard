<template>
  <div class="w-full h-auto flex flex-col items-center justify-center bg-[#fafafa]">
    <NavbarCmp />
    <MainBody />
    <FooterCmp />
  </div>
</template>

<script>
import NavbarCmp from './components/NavbarCmp.vue';
import MainBody from './components/MainBody.vue';
import FooterCmp from './components/FooterCmp.vue';

export default {
  name: 'App',
  components: {
    NavbarCmp,
    MainBody,
    FooterCmp,
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
