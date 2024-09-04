<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router';
import HelloWorld from '../../src/components/HelloWorld.vue';
import VueFlow from '../../src/views/VueFlow/index.vue';
</script>

<template>
  <div class="about">
    <h1>This is an about page</h1>
    <!-- <HelloWorld msg="You did it!" /> -->
    <VueFlow></VueFlow>
  </div>
</template>

<style>
@media (min-width: 1024px) {
  .about {
    width: 1500px;
    width: 2000px;
  }
}
</style>
