<template>
  <div>
    <h1 v-text="msg" 
    ref="title"></h1>
    <button ref="btn"  
    @click="show">展示DOm</button>
    <School ref="sch"></School>
    <Student studentName="张三" v-bind:age="20"></Student>
    
  </div>
</template>

<script>
import { component } from 'vue/types/umd';
import School from './components/School1.vue';
import Student from './components/Student1.vue';
export default {
name:'App',
  components:{
    School,
    Student,
  },
};
</script>

<style>

</style>