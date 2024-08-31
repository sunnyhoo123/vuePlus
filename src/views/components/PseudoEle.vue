<script setup lang="ts">
import { nextTick, onMounted } from 'vue'

onMounted(() => {})
</script>

<template>
  <div class="about">
    <div
      id="div1"
      style="
        position: absolute;
        top: 50px;
        left: 50px;
        width: 100px;
        height: 100px;
        background-color: lightblue;
      "
    ></div>
    <div
      id="div2"
      style="
        position: absolute;
        top: 50px;
        left: 300px;
        width: 100px;
        height: 100px;
        background-color: lightcoral;
      "
    ></div>
  </div>
</template>

<style scoped>
#div1::after {
  content: '';
  position: absolute;
  top: 50%;
  left: 100%;
  width: 200px; /* div1 和 div2 之间的距离 */
  height: 2px;
  background-color: black;
}
</style>
