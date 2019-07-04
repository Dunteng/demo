<template>
  <div class="addStudent">
    添加学生：
    <input type="text" v-model="name" />
    <button @click="addStu">添加</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      name: ""
    };
  },
  methods: {
    addStu() {
      this.$emit("add", this.name); //子组件向父组件派发一个方法，子组件向父组件传值
      //注意这个this.$emit的this不能没写
    }
  }
};
</script>   

<style scoped>
</style>