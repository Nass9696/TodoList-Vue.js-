<template>
  <div>
    <TodoInputTextVue v-model="newTodoText" @keydown.enter="addToDo" />
    <TodoListItem v-bind:todos="todos" />
  </div>
</template>

<script>
import TodoInputTextVue from "@/components/TodoInputText.vue";
import TodoListItem from "@/components/TodoListItem.vue";

export default {
  components: {
    TodoInputTextVue,
    TodoListItem
  },
  data() {
    return {
      newTodoText: "",
      todos: ["Try", "Test", "Stories"]
    };
  },
  methods: {
    addToDo() {
      const trimmedText = this.newTodoText.trim();
      if (trimmedText) {
        this.todos.push(trimmedText);
        this.newTodoText = "";
      }
    }
  }
};
</script>

<style>
</style>