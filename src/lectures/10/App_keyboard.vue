<template>
  <div>
    <input type="text" @keyup.enter="addTodo" />
    <ul>
      <li v-for="(todo, index) in todos" :keys="index">
        {{ todos }}
      </li>
    </ul>
  </div>
</template>

<script>
import { reactive } from 'vue'
export default {
  setup() {
    const todos = reactive([])

    const addTodo = (event) => {
      if (event.key === 'Enter') {
        todos.push(event.target.value)
      }
    }
    return {
      todos,
      addTodo
    }
  }
}
</script>

<style lang="scss" scoped></style>
