<template>
  <div>
    <TodoInputTextVue v-on:todos="todos" />
  </div>
</template>

<script>
import TodoInputTextVue from "@/components/TodoInputText.vue";
export default {
  components: {
    TodoInputTextVue
  },
  data() {
    return {
      todos: ["Afa", "Doflex", "Stories"]
    };
  }
};
</script>

<style>
</style>