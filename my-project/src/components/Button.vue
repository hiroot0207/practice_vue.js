<template>
  <div>
    <h2>
      <input type="submit" @click="count">
      <p>The button above has been clicked {{ counter }} times.</p>
    </h2>
  </div>
</template>

<script>
export default {
  data () {
    count: null
  },
  methods: {
    count () {
      return count += 1
    }
  }
}

//  props: ['input1', 'input2'],
//  computed: {
//    sum () {
//      return Number(this.input1) + Number(this.input2)
//    }
//  }

</script>

<style scoped>
  h1 {
    color : green
  }
</style>
