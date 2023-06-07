<template>
 <div class="demo2">
        <h4>姓名:{{name}}</h4>
        <h4>年龄:{{sex}}</h4>   
    </div>
</template>
<script>
//组件的交互，数据和方法
export default {
    name:'Student',
     data() {
        return{
            studentname:'张三',
            sex:'女',
        };
     },
    
    };
</script>

<style>
/*组件的样式*/
.demo2{
background-color: yellow;
}
</style>