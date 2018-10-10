<template>
  <div>
    <h1>
      <br>
      <input type="text" v-model="num1">
      <input type="text" v-model="num2">
      <br>
      input1 = {{ input1 }}
      <br>
      input2 = {{ input2 }}
      <br>
      sum = {{ sum }}
    </h1>
    </div>
</template>

<script>
export default {
  props: ['input1', 'input2'],
  computed: {
    sum () {
      return Number(this.input1) + Number(this.input2)
    }
  }
}
</script>

<style scoped>
  h1 {
    color : green
  }
</style>
