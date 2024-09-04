<script setup lang="ts">
import { nextTick, onMounted } from 'vue';
import { watch, ref } from 'vue';
const value = ref<string>('');
const value1 = ref<string>('');
watch(value, () => {
  console.log(value.value);
});
watch(value1, () => {
  console.log(value1.value);
});
onMounted(() => {});
</script>

<template>
  <div class="pseudo-ele">
    <svg width="600" height="100">
      <rect
        x="10"
        y="20"
        width="150"
        height="50"
        fill="#f0f0f0"
        stroke="#000"
      />
      <text x="35" y="50" fill="black">Component A</text>

      <line x1="160" y1="45" x2="210" y2="45" stroke="black" stroke-width="2" />

      <rect
        x="210"
        y="20"
        width="150"
        height="50"
        fill="#f0f0f0"
        stroke="#000"
      />
      <text x="235" y="50" fill="black">Component B</text>

      <line x1="360" y1="45" x2="410" y2="45" stroke="black" stroke-width="2" />

      <rect
        x="410"
        y="20"
        width="150"
        height="50"
        fill="#f0f0f0"
        stroke="#000"
      />
      <text x="435" y="50" fill="black">Component C</text>
    </svg>
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
    >
      <a-input v-model:value="value" placeholder="Basic usage" />
    </div>
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
    >
      <a-input v-model:value="value" placeholder="Basic usage" />
    </div>
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
