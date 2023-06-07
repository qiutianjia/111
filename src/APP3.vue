<template>
 <div> 
    <p>父子组件通信，父组件msg值:{{msg}}</p>
    <child-componet
    :message="msg"
    v-on:getChlidData="getData"></child-componet>
    </div>
</template>
<script>
//组件的交互，数据和方法
import childComponet from './components/childComponent.vue';
export default {
    components:{
      childComponet,
    },
    data(){
   return{
    msg:'',
     };
    },
     methods:{
        getDate(val){
         this.msg = val;
        },
     },
     
    };
</script>

<style>

</style>