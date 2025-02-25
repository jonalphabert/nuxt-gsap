<template>
  <div class="container flex items-center justify-center h-screen w-screen -mx-auto">
    <div ref="box" class="box">
      Hello, GSAP!
    </div>
  </div>
</template>

<script setup>
import {ref, onMounted} from 'vue';

// Access GSAP via the global plugin
const {$gsap} = useNuxtApp();
const box = ref(null);

onMounted(() => {
  // Animate the box using GSAP
  $gsap.to(box.value, {
    x: 200,
    rotation: 360,
    duration: 2,
    ease: 'power2.out',
  });
});
</script>

<style scoped>
.box {
  width: 100px;
  height: 100px;
  background-color: #42b983;
  display: flex;
  align-items: center;
  justify-content: center;
  color: white;
  font-weight: bold;
}
</style>