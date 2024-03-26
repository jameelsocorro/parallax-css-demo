<script setup>
import ParallaxHero from './components/ParallaxHero.vue'
</script>

<template>
  <main>
    <ParallaxHero />
    <div class="content"></div>
  </main>
</template>

<style>
.content {
  position: relative;
  z-index: 10;
  background-color: #2d112b;
  height: 2000px;
}
</style>
