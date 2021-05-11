<template>
  <div >
    <div class="title">SimpleCalculator</div>
    <div class="calculator">
      <div class="display"></div>
      <div class="btn">7</div>
      <div class="btn">8</div>
      <div class="btn">9</div>
      <div class="operator">C</div>
      <div class="btn">4</div>
      <div class="btn">5</div>
      <div class="btn">6</div>
      <div class="operator">-</div>
      <div class="btn">1</div>
      <div class="btn">2</div>
      <div class="btn">3</div>
      <div class="operator">+</div>
      <div class="btn zero">0</div>
      <div class="operator">=</div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'SimpleCalculator',
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.title {
  margin-bottom: 8px;
}
.calculator {
  margin: 0 auto;
  width: 400px;
  font-size: 40px;
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  grid-auto-rows: minmax(50px, auto);
}
.display {
  grid-column: 1 / 5;
  background-color: #333;
  color: white;
}
.btn {
  background-color: #eee;
  border: 1px solid #999;
}
.zero {
  grid-column: 1 / 4;
}
.operator {
  background-color:steelblue;
  border: 1px solid #999;
}
</style>
