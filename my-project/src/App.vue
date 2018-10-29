<template>
  <div>
    <div>
      {{msg}}
      <br>
      <Todo @todoaction="done" />
    </div>
    <div>
      実施済タスク：{{ counter1 }}
    </div>
  </div>
</template>

<script>
import Todo from './components/Todo'
export default {
  name: 'App',
  components: {
    Todo
  },
  data () {
    return {
      msg: 'ToDo List',
      counter1: 0
    }
  },
  methods: {
    done () {
      this.counter1 = Number(this.counter1) + 1
    }
  }
}
</script>

<style scoped>
  div {
    color : black
  }
</style>
