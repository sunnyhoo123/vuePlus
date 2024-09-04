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

onMounted(() => {
  nextTick();
  const a = document.getElementById('a'),
    b = document.getElementById('b'),
    c = document.getElementById('c');

  const line1 = new LeaderLine(a, b, {
    color: 'red', //线的颜色
    size: 8, //线的粗细
    dash: true, // 虚线 dash:[2,4]
    endPlug: 'hand', // 线尾类型
    endPlugSize: 1, // 线尾尺寸
    startPlug: 'disc', // 线头类型
    startPlugSize: 2, //线头尺寸
    path: 'grid', // 线的类型
    // 更多配置可参见文档
  });
  const line2 = new LeaderLine(a, c);
});
</script>

<template>
  <div id="leader-line" class="leader-line">
    <div>
      <div
        id="a"
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
        id="b"
        style="
          position: absolute;
          top: 200px;
          left: 300px;
          width: 100px;
          height: 100px;
          background-color: lightcoral;
        "
      ></div>
      <div
        id="c"
        style="
          position: absolute;
          top: 200px;
          left: 500px;
          width: 100px;
          height: 100px;
          background-color: lightcoral;
        "
      ></div>
    </div>
  </div>
</template>

<style>
.leader-line {
  position: relative;
}
</style>
