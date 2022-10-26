<template>
  <form @submit.prevent="addItemAndClear(todo)">
    <input v-model="todo" type="text" /><button>Add</button>
  </form>
</template>

<script setup lang="ts">
import { ref } from "vue";
import { useTodoListStore } from "@/stores/useTodoListStore";

const todo = ref("");
const store = useTodoListStore()

function addItemAndClear(item: string) {
  if (item.length === 0) {
    return;
  }
  store.addTodo(item);
  todo.value = "";
}
</script>

<style lang="scss"></style>