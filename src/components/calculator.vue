<template>
  <div>
    <input type="text" v-model="numberOne">
    <select v-model="operand">
      <option value="+">+</option>
      <option value="-">-</option>
      <option value="/">/</option>
      <option value="*">*</option>
    </select>
    <input type="text" v-model="numberTwo">
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
      numberOne : 0,
      numberTwo : 0,
      operand : '+',
    }
  },
  computed : {
    result() {
      switch (this.operand) {
        case "+" :
          return (+(this.numberOne) + +(this.numberTwo));
        case "-" :
          return ((this.numberOne) - (this.numberTwo));
        case "*" :
          return ((this.numberOne) * (this.numberTwo));
        case "/" :
          return ((this.numberOne) / (this.numberTwo));
        default:
          return 0
      }
    }
  }
}
</script>

<style scoped>

</style>