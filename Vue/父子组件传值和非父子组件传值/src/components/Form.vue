<template>
  <div class="form">
    <h3>我是addStudent组件和StudentList组件的父组件</h3>

    <add-student @add="addFunc"></add-student>
    <hr />
    <student-list :student="studentList"></student-list>
  </div>
</template>

<script>
import StudentList from "./StudentList";
import addStudent from "./addStudent";
export default {
  data() {
    return {
      studentList: []
    };
  },
  methods: {
    addFunc(param) {
      console.log(param);
      this.studentList.push(param);
      //   console.log(this.studentList);
    }
  },
  components: {
    StudentList,
    addStudent
  }
};
</script>

<style scoped>
</style>