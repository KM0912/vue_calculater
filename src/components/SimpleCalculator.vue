<template>
  <div >
    <div class="title">SimpleCalculator</div>
    <div class="calculator">
      <div class="display">{{ inputNum || '0' }}</div>
      <div v-on:click="append('7')" class="btn">7</div>
      <div v-on:click="append('8')" class="btn">8</div>
      <div v-on:click="append('9')" class="btn">9</div>
      <div class="operator">C</div>
      <div v-on:click="append('4')" class="btn">4</div>
      <div v-on:click="append('5')" class="btn">5</div>
      <div v-on:click="append('6')" class="btn">6</div>
      <div class="operator">-</div>
      <div v-on:click="append('1')" class="btn">1</div>
      <div v-on:click="append('2')" class="btn">2</div>
      <div v-on:click="append('3')" class="btn">3</div>
      <div class="operator">+</div>
      <div v-on:click="append('0')" class="btn zero">0</div>
      <div class="operator">=</div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'SimpleCalculator',
  data() {
    return {
      inputNum: '',
    }
  },
  methods: {
    append(number) {
      // 入力済みの値が''(空)で入力値が0の場合は何もせずに終了
      if (this.inputNum == '' && number == 0) {
        return
      }
      this.inputNum = `${this.inputNum}${number}`
    }
  }
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
  background-color: steelblue;
  border: 1px solid #999;
}
</style>
