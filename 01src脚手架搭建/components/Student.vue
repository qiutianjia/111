<template>
 <div>
        <h4>姓名:{{studentname}}</h4>
        <h4>年龄:{{age}}</h4>   
    </div>
</template>
<script>
//组件的交互，数据和方法
export default {
    name:'Student',
     data() {
        return{
            studentname:'张三',
        age:18,
        };
     },
     methods:{
        show(){
            console.log('@@@');
        }
     }
    };
</script>

<style>
/*组件的样式*/

</style>