<template>
  <div>
    <div>
      <br>
      新規追加
      <br>
      <input type="text" v-model="input1">
      <br>
      <input type="date" v-model="input2">
      <input type="submit" value="追加" @click="addTodo">
      <br>
      <ul>
        <li v-for="(todo, index) in todolist" v-bind:key="todo">
          {{todo.name}}
          {{todo.duedate}}
          <input type="submit" value="完了" @click="removeTodo(index); $emit('todoaction')">
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Todo',
  data () {
    return {
      input1: null,
      input2: null,
      todolist: []
    }
  },
  methods: {
    addTodo () {
      this.todolist.push(
        {
          name: this.input1,
          duedate: this.input2
        }
      )
    },
    removeTodo (index) {
      this.todolist.splice(index, 1)
    }
  }
}
</script>

<style scoped>
  div {
    color : darkgreen
  }
</style>
