<script>
import Todo from './components/Todo.vue';
import InputTodo from './components/InputTodo.vue';
import Complate from './components/Complate.vue';
export default {
  data() {
    return {
      todoList: ['dayouxi', 'xuexi'],
      complateList: ['', ''],
    };
  },
  components: {
    Todo,
    InputTodo,
    Complate,
  },
};
</script>

<template>
  <div class="all">
    <InputTodo />
    <Todo v-for="todo in todoList" :todo="todo" />
    <Complate
      :countAll="todoList.length"
      :countComplate="complateList.length"
    />
  </div>
</template>

<style scoped>
.inputTodo {
  margin-bottom: 60px;
}
.all {
  border: 1px solid #ccc;
  padding: 20px;
  border-radius: 10px;
}
.complate {
  padding-top: 50px;
}
</style>
