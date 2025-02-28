<template>
  <div class="bg-red-50">
    <div class="max-w-[420px] w-screen mx-auto">
      <div class="h-screen bg-[#C7CEB9]">
        <div class="grid grid-cols-6 ">
          <div class="text-wrap py-2 px-2">
            <h1 class="uppercase text-4xl rotate-270">E</h1>
            <h1 class="uppercase text-4xl rotate-270">S</h1>
            <h1 class="uppercase text-4xl rotate-270">O</h1>
            <h1 class="uppercase text-4xl rotate-270">R</h1>
            <h1 class="uppercase text-4xl rotate-270"> </h1>
            <h1 class="uppercase text-4xl rotate-270">E</h1>
            <h1 class="uppercase text-4xl rotate-270">C</h1>
            <h1 class="uppercase text-4xl rotate-270">I</h1>
            <h1 class="uppercase text-4xl rotate-270">L</h1>
            <h1 class="uppercase text-4xl rotate-270">A</h1>
          </div>
          <div class="col-span-4 h-screen relative">
            <div class="flex flex-col justify-between h-screen py-[10vh] px-4">
              <h2 class="text-3xl relative z-10">The Wedding</h2>
              <div class="relative z-10">
                <p>Kepada : John Doe</p>
                <p>Undangan untuk 2 orang</p>
              </div>
            </div>

            <div class="absolute bottom-0 w-full">
              <img src="/images/test-image.png" class="h-[90vh] w-full" alt="cover"/>
            </div>
          </div>
          <div class="text-wrap flex flex-col justify-end py-2 px-2">
            <h1 class="uppercase text-4xl rotate-270 text-center groom-name">E</h1>
            <h1 class="uppercase text-4xl rotate-270 text-center groom-name">S</h1>
            <h1 class="uppercase text-4xl rotate-270 text-center groom-name">O</h1>
            <h1 class="uppercase text-4xl rotate-270 text-center groom-name">R</h1>
            <h1 class="uppercase text-4xl rotate-270 text-center groom-name"> </h1>
            <h1 class="uppercase text-4xl rotate-270 text-center groom-name">E</h1>
            <h1 class="uppercase text-4xl rotate-270 text-center groom-name">C</h1>
            <h1 class="uppercase text-4xl rotate-270 text-center groom-name">I</h1>
            <h1 class="uppercase text-4xl rotate-270 text-center groom-name">L</h1>
            <h1 class="uppercase text-4xl rotate-270 text-center groom-name">A</h1>
          </div>
        </div>
      </div>
      <div class="text-center py-12 px-6">
        <h3>Fil. 1:4</h3>
        <p>
          Aku mengucap syukur kepada Allah-ku, setiap kali aku mengingat engkau dalam doaku
        </p>
      </div>
      <div class="py-12 px-6">
        <div class="grid grid-cols-2 gap-4 mb-4">
          <div>
            <img src="/images/test-image.png" class="w-full aspect-auto" alt="cover"/>
          </div>
          <div class="flex flex-col justify-center">
            <h4 class="text-2xl font-bold mb-2">Alice Rose</h4>
            <p class="text-base">Putra Pertama dari Bapak David dan Ibu Abigail</p>
          </div>
        </div>
        <div class="grid grid-cols-2 gap-4">
          <div class="flex flex-col justify-center">
            <h4 class="text-2xl font-bold mb-2">Alice Rose</h4>
            <p class="text-base">Putra Pertama dari Bapak David dan Ibu Abigail</p>
          </div>
          <div>
            <img src="/images/test-image.png" class="w-full aspect-auto" alt="cover"/>
          </div>
        </div>
      </div>
      <div class="relative py-12">
        <h3 class="uppercase text-4xl font-bold absolute top-6 -right-2 tracking-wide">Save The Date</h3>
        <div class="py-12">
          <h4 class="mb-4 text-lg font-semibold text-center">Pemberkatan</h4>
          <div class="flex text-2xl mx-auto justify-center gap-8">
            <p class="text-center">24 Sep 2025</p>
            <div class="w-1 h-full bg-red-500 px-2"></div>
            <p class="text-center">12.00 WIB</p>
          </div>
        </div>

      </div>
    </div>
  </div>
</template>

<script setup>
import {ref, onMounted} from 'vue';

const {$gsap} = useNuxtApp();
const params = useRoute()

onMounted(() => {
  $gsap.to(".groom-name", {
    duration: 1,
    x: -10,
    stagger:{
      each: 0.2,
      from:'end',
    },
    repeat: -1,
    yoyo: true,
  })
});
</script>