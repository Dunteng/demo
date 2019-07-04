<template>
  <div class="StudentList">
    学生列表：
    <ul>
      <li v-for="(item,index) in student" :key="index+item">{{item}}</li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {};
  },
  //   props: ["student"]  //简易写法
  props: {
    student: {
      type: Array,
      default: ""
    }
  }
};
</script>

<style scoped>
</style>