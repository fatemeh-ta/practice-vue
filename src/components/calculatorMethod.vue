<template>
  <div>
    <input type="text" v-model="numberOne">
    <select v-model="operand">
      <option value="+">+</option>
      <option value="-">-</option>
      <option value="*">*</option>
      <option value="/">/</option>
    </select>
    <input type="text" v-model="numberTwo">
    <button @click.prevent="resultMethod()">calculator</button>
    <span> 
      result is :
      {{ result }}
    </span>
  </div>
</template>

<script>
export default {
  data() {
    return {
      numberOne : "0",
      numberTwo : "0",
      operand : "*",
      result : 0
    }
  },
  methods : {
    resultMethod() {
      // if (this.operand === "+") {
      //   this.result = +this.numberOne + +this.numberTwo;
      // } else if (this.operand === "-") {
      //   this.result = this.numberOne - this.numberTwo;
      // } else if (this.operand === "*") {
      //   this.result = this.numberOne * this.numberTwo;
      // } else if (this.operand === "/") {
      //   this.result = this.numberOne / this.numberTwo;
      // } 
      switch (this.operand) {
        case "+":
          this.result = +this.numberOne + +this.numberTwo
          break;
        case "-":
          this.result = this.numberOne - this.numberTwo
          break;
        case "*":
          this.result = this.numberOne * this.numberTwo
          break;
        case "/":
          this.result = this.numberOne / this.numberTwo
        break;
        default:
          break;
      }
    }
  }
}
</script>

<style scoped>

</style>