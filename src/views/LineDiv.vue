<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
import SvgDiv from './components/SvgDiv.vue'
import PseudoEle from './components/PseudoEle.vue'
import CanvasDiv from './components/CanvasDiv.vue'
import LeaderLine from './components/LeaderLine.vue'
</script>

<template>
  <div class="about">
    <h1>This is an about page</h1>
    <SvgDiv></SvgDiv>
    <PseudoEle></PseudoEle>
    <LeaderLine></LeaderLine>
  </div>
</template>

<style scoped>
@media (min-width: 1024px) {
  .about {
    min-height: 100vh;
    display: flex;
    align-items: center;
  }
}
</style>
