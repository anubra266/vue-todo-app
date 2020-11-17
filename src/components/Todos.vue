<template>
  <div>
    <div v-for="todo in todos" :key="todo.id">
      <TodoItem :todo="todo" v-on:del-todo="$emit('del-todo', todo.id)" />
    </div>
  </div>
</template>

<script>
import TodoItem from "./TodoItem";
export default {
  name: "todos",
  props: ["todos"],
  components: { TodoItem },
};
</script>

<style scoped></style>
