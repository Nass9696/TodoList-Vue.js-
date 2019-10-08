<template>
  <div>
    <TodoInputTextVue @keydown.enter="addToDo" />
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
      todos: ["Try", "Test", "Stories"]
    };
  },
  methods: {
    addToDo() {
      alert("test");
    }
  }
};
</script>

<style>
</style>