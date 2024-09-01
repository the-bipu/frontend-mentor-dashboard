<template>
  <div class="w-full flex flex-col items-center justify-center border-b border-[#dbe5e6]">
    <header class="w-11/12 h-20 flex flex-row justify-between items-center">

      <div class="flex flex-row gap-4 barlow">
        <img src="../assets/logo-desktop.svg" alt="" class="h-9 p-1">
      </div>
      <div class="flex flex-row gap-2.5 items-center justify-center">
        <p class="font-semibold italic text-[15px] tracking-wider uppercase text-black barlow flex items-center mr-5 cursor-pointer">Profile</p>
        <img src="../assets/profile.jpeg" alt="" class="w-10 h-10 rounded-full cursor-pointer">
        <img src="../assets/arrow-down.png" alt="" class="h-3.5 transition-all cursor-pointer hover:rotate-180">
      </div>

    </header>
  </div>
  <div class="w-full flex flex-row items-center justify-center border-b border-[#dbe5e6] sticky top-0 bg-[#fafafa] z-50">
    <div class="w-11/12 flex flex-row items-center justify-between text-center">
      <div class="font-semibold tracking-wider uppercase text-black barlow border-x border-[#dbe5e6] py-4 px-6 flex items-center">
        challenges
      </div>
      <div class="font-semibold tracking-wider uppercase text-black barlow border-x border-[#dbe5e6] py-4 px-6 flex items-center">
        💌 lob
      </div>
    </div>
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
