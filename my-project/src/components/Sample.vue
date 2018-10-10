<template>
  <div>
    <h1>
      <br>
      <input type="text" v-model="num1">
      <input type="text" v-model="num2">
      <br>
      {{ input1 }}
      {{ input2 }}
      {{ sum }}
    </h1>
    </div>
</template>

<script>
export default {
  props: ['input1', 'input2'],
  computed: {
    sum () {
      console.log(Number(this.input1))
      if (Number(this.input1) > Number(this.input2)) {
        return 'input1 > input2'
      } else if (Number(this.input1) < Number(this.input2)) {
        return 'input1 < input2'
      } else {
        return 'input1 = input2'
      }
    }
  }
}
</script>

<style scoped>
  h1 {
    color : green
  }
</style>
