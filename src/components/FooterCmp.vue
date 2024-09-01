<template>
    <div class="w-full flex flex-col items-center justify-center bg-white">
        <header class="w-11/12 h-auto py-20 flex flex-row justify-between items-center">

            <div class="flex flex-row gap-4 barlow">
                <img src="../assets/logo-desktop.svg" alt="" class="h-9 p-1">
            </div>
            <div class="flex flex-row gap-2.5 items-center justify-center">
                <img src="../assets/profile.jpeg" alt="" class="w-10 h-10 rounded-full cursor-pointer">
                <img src="../assets/profile.jpeg" alt="" class="w-10 h-10 rounded-full cursor-pointer">
                <img src="../assets/profile.jpeg" alt="" class="w-10 h-10 rounded-full cursor-pointer">
                <img src="../assets/profile.jpeg" alt="" class="w-10 h-10 rounded-full cursor-pointer">
            </div>

        </header>
    </div>
    <div
        class="w-full flex flex-row items-center justify-center border-t border-[#dbe5e6] sticky top-0 bg-[#ffffff] z-50">
        <div class="w-11/12 flex flex-row items-center justify-between text-center">
            <div
                class="font-normal tracking-wider uppercase text-base text-[#737373] barlow py-4 px-6 flex items-center">
                Frontend Mentor Solutions 2023 - 2024
            </div>
            <div
                class="font-normal tracking-wider uppercase text-base text-[#737373] barlow py-4 px-6 flex items-center">
                Made with 💌 lob by @the-bipu
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'FooterCmp',
};
</script>