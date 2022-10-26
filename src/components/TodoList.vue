<template>
  <div class="list" v-for="todo in todoList" :key="todo.id">
    <div :class="{ completed: todo.completed } + ' list-item'">
      {{ todo.item }}
    </div>
    <div class="list-action">
      <span @click.stop="toggleCompleted(todo.id)">&#10004;</span>
      <span @click="deleteTodo(todo.id)">&#10060;</span>
    </div>
  </div>
</template>

<script setup lang="ts">
import { useTodoListStore } from "@/stores/useTodoListStore";
import { storeToRefs } from "pinia";

const store = useTodoListStore();
const { todoList } = storeToRefs(store);
const { toggleCompleted } = store;
const { deleteTodo } = store;
</script>

<style lang="scss">
.completed {
  text-decoration: line-through;
}
.list {
  display: flex;
  justify-content: space-around;
  align-items: center;
  flex-direction: row;
}
</style>
