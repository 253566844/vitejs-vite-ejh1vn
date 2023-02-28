<script>
export default {
  data() {
    return {
      allChecked: false,
    };
  },
  props: ['countComplate', 'countAll'],
};
</script>

<template>
  <div align="left" class="complate" id="complate">
    <input id="allChecked" type="checkbox" v-model="allChecked" />
    <span class="count">已完成{{ countComplate }}/全部{{ countAll }}</span>
  </div>
</template>

<style scoped>
.count {
  margin-left: 20px;
}
</style>
