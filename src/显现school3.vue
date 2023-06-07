<template>
  <div>
    <h1 class="demo">欢迎你</h1>
    <School/>
    <Student/>
    
  </div>
</template>

<script>
import School from './components/School3.vue';
import Student from './components/Student3.vue';
export default {
name:'App',
  components:{
    School,
    Student,
  },
};
</script>

<style scoped>
.demo{
  color: red;
}
</style>