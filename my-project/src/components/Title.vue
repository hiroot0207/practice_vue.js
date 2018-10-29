<template>
  <h1>
    <h3>{{ title }}</h3>
    <input type="text" v-model="input1">
    <input type="text" v-model="input2">
    {{ goukei }}
  </h1>
</template>

<script>
export default {
  name: 'Title',
  props: ['title'],
  data () {
    return {
      input1: 0,
      input2: 0
    }
  },
  computed: {
    goukei () {
      return this.input1 + this.input2
    }
  }
}
</script>

<style scoped>
h1 {
  color:tomato
}
</style>
