<template>
 <div>
        <h4 @click="show">姓名:{{name}}</h4>
        <h4>性别:{{sex}}</h4>   
    </div>
</template>
<script>
import { hunru,hunru2 } from '../aaa';
//组件的交互，数据和方法
export default {
    name:'Student',
     data() {
        return{
           name:'李四',
           sex:'女',
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

<style>
/*组件的样式*/

</style>