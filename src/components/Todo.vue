<script>
export default {
  data() {
    return {
      showButton: false,
      deleteTodo: true,
      allTodo: [],
    };
  },
  props: ['todo'],
};
</script>

<template>
  <div
    v-if="deleteTodo"
    @mouseover="this.showButton = true"
    @mouseout="this.showButton = false"
  >
    <div align="left" id="todo">
      <div class="checkboxTodo">
        <input id="checkbox" type="checkbox" v-model="allTodo" />
        <label for="checkbox">{{ todo }}</label>
      </div>
      <div align="right" v-show="showButton" class="deleteButton">
        <button @click.prevent="deleteTodo = false">删除</button>
      </div>
    </div>
  </div>
</template>

<style scoped>
#todo {
  height: 40px;
  width: 600px;
  border: solid #ccc 1px;
  font-size: 20px;
  border-radius: 5px;
  padding-top: 6px;
  margin-bottom: -0.5px;
}
#todo:hover {
  height: 40px;
  width: 600px;
  border: solid #ccc 1px;
  font-size: 20px;
  padding-top: 6px;
  border-radius: 5px;
  background: #dcdcdc;
}
input[type='checkbox'] {
  margin-right: 8px;
}
.checkboxTodo {
  width: 50%;
  height: 100%;
  display: inline-block;
}
.deleteButton {
  width: 50%;
  height: 100%;
  display: inline-block;
}
button {
  height: 70%;
  font-size: 10px;
  background: #ff4d5d;
  color: white;
  margin-right: 10px;
  font-weight: 700;
  outline: none;
}
button:active {
  height: 70%;
  font-size: 10px;
  background: #af2430;
  color: white;
  margin-right: 10px;
  font-weight: 700;
  outline: none;
}
</style>
