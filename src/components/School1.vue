<template>
 <div>
        <h4  @click="show">学校:{{name}}</h4>
        <h4>地址:{{address}}</h4>   
    </div>
</template>
<script>
// //在在使用混入的时候，如果自己本身有的属性以自己的数值为主，
// 自己没有的接收混合送来的。原则：
// 以自己的为主。
import { hunru,hunru2 } from '../aaa';
//组件的交互，数据和方法
export default {
    name:'School',
     data() {
        return{
            name:'山东商务',
            address:'烟台',
            a:888,
        };
     },
     methods:{
        show(){
            alert(this.name);
        },
     },
     mixins:[hunru,hunru2],
    };
</script>
// (await import('vue')).defineComponent 
<style>
</style>