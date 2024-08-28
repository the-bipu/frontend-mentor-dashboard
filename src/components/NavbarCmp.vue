<template>
  <div class="w-full flex flex-col items-center justify-center shadow">
    <header class="w-10/12 h-20 flex flex-row justify-between items-center">

      <div class="flex flex-row gap-4 barlow">
        <img src="../assets/logo-desktop.svg" alt="" class="h-10 p-1">
      </div>
      <div class="flex flex-row gap-2.5 items-center">
        <img src="../assets/profile.jpeg" alt="" class="w-10 h-10 rounded-full">
        <img src="../assets/arrow-down.png" alt="" class="h-3.5 hover:rotate-180">
      </div>

    </header>
  </div>
</template>

<script>
export default {
  name: 'NavbarCmp',
  props: {
    msg: String
  },
  methods: {
    click() {
      document.querySelector(".main-menu").classList.toggle("show-menu");
    },
    removeMenu() {
      document.querySelector(".main-menu").classList.remove("show-menu");
    },
  },
};
</script>
