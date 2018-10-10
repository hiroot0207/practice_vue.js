<template>
  <div>
    <div>
    {{msg}}
    <br>
    <br>
    新規追加
    <br>
      <input type="text">
      <input type="submit" value="追加">
      <br>
    </div>
    <div>
      <input type="button" value="追加" @click="plus">
      <input type="button" value="削除" @click="minus">
    </div>
    <div id="todoarea"></div>
    <div>
      <br>
      <Todo task='スーツを買う' @todoaction="done" />
      <Todo task='革靴を買う' @todoaction="done" />
    </div>
    <div>
      実施済：{{ counter1 }}
      <br>
      未着手：{{ counter2 }}
      <input type="submit" @click="done">
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
      counter1: 0,
      counter2: 0
    }
  },
  methods: {
    done () {
      this.counter1 = Number(this.counter1) + 1
      this.counter2 = Number(this.counter2) - 1
    },
    plus () {
      const todoarea = document.getElementById('todoarea')
      const p1 = document.createElement('p')
      const text1 = document.createTextNode('テスト')
      p1.appendChild(text1)
      todoarea.appendChild(p1)
    },
    minus () {
      const todoarea = document.getElementById('todoarea')
      todoarea.removeChild(todoarea.firstChild)
    }
  }
}
</script>

<style scoped>
  div {
    color : black
  }
</style>
