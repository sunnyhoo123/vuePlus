<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router';
import HelloWorld from '../../src/components/HelloWorld.vue';
import { nextTick, onMounted } from 'vue';

onMounted(() => {
  nextTick();
  const div1 = document.getElementById('div1');
  const div2 = document.getElementById('div2');
  const line = document.getElementById('line');

  // 获取 div 的中心点
  const rect1 = div1.getBoundingClientRect();
  const rect2 = div2.getBoundingClientRect();

  const x1 = rect1.left + rect1.width / 2;
  const y1 = rect1.top + rect1.height / 2;
  const x2 = rect2.left + rect2.width / 2;
  const y2 = rect2.top + rect2.height / 2;

  // 设置线的起点和终点
  line.setAttribute('x1', x1);
  line.setAttribute('y1', y1);
  line.setAttribute('x2', x2);
  line.setAttribute('y2', y2);
});
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
        top: 200px;
        left: 300px;
        width: 100px;
        height: 100px;
        background-color: lightcoral;
      "
    ></div>

    <svg height="500" width="500" style="position: absolute; top: 0; left: 0">
      <line
        id="line"
        x1="0"
        y1="0"
        x2="0"
        y2="0"
        style="stroke: rgb(99, 99, 99); stroke-width: 2"
      />
    </svg>
  </div>
</template>

<style>
@media (min-width: 1024px) {
  .about {
    min-height: 100vh;
    display: flex;
    align-items: center;
  }
}
</style>
