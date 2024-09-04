<script setup lang="ts">
import { nextTick, onMounted } from 'vue';

onMounted(() => {
  nextTick();
  const canvas = document.getElementById('canvas');
  const ctx = canvas.getContext('2d');

  const div1 = document.getElementById('div3');
  const div2 = document.getElementById('div4');
  const div0 = document.getElementById('canvas-div');

  // 设置 canvas 大小
  canvas.width = window.innerWidth;
  canvas.height = window.innerHeight;

  // 获取 div 的中心点
  const rect1 = div1.getBoundingClientRect();
  const rect2 = div2.getBoundingClientRect();

  const x1 = rect1.left + rect1.width / 2;
  const y1 = rect1.top + rect1.height / 2;
  const x2 = rect2.left + rect2.width / 2;
  const y2 = rect2.top + rect2.height / 2;

  // 绘制线
  ctx.beginPath();
  ctx.moveTo(x1, y1);
  ctx.lineTo(x2, y2);
  ctx.stroke();
});
</script>

<template>
  <div id="canvas-div" class="canvas-div">
    <canvas id="canvas" style="position: absolute; top: 0; left: 0"></canvas>

    <div
      id="div3"
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
      id="div4"
      style="
        position: absolute;
        top: 200px;
        left: 300px;
        width: 100px;
        height: 100px;
        background-color: lightcoral;
      "
    ></div>
  </div>
</template>

<style>
.canvas-div {
  position: relative;
}
</style>
