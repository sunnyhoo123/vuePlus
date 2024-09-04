<template>
  <div class="flow-container">
    <div class="component">Component A</div>
    <div class="arrow">→</div>
    <div class="component">Component B</div>
    <div class="arrow">→</div>
    <div class="component">Component C</div>
  </div>
</template>

<style>
.flow-container {
  display: flex;
  align-items: center;
}
.component {
  padding: 10px 20px;
  border: 1px solid #000;
  margin: 0 10px;
  background-color: #f0f0f0;
}
.arrow {
  font-size: 24px;
}
</style>
