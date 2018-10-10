<template>
    <div>
      ・{{ task }}
    <input type="submit" value="完了" @click="$emit('todoaction')">
    </div>
</template>

<script>
export default {
  name: 'Todo',
  props: ['task'],
  data () {
    return {
    }
  }
}
</script>

<style scoped>
  div {
    color : orange
  }
</style>
