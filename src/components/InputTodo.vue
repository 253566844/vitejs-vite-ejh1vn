<script>
export default {
  data() {
    return {
      showButton: false,
      deleteTodo: true,
    };
  },
  method: {
    inputTodoList() {
      alert('ssssss');
    },
  },
};
</script>

<template>
  <input
    id="inputTodo"
    placeholder="请输入你的任务名，按回车键确认"
    class="inputTodo"
    type="text"
    @keyup.enter="inputTodoList"
  />
</template>

<style scoped>
.inputTodo {
  height: 40px;
  width: 596px;
  border-radius: 5px;
  border: 1px solid #ccc;
  font-size: 20px;
  box-shadow: 0px 0px 5px 2px #ccc;
}
.inputTodo:focus {
  height: 40px;
  width: 596px;
  border-radius: 5px;
  border: 1px solid #4dafff;
  font-size: 20px;
  box-shadow: 0px 0px 5px 2px #4dafff;
  outline: none;
}
</style>
