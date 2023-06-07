<template>
 <div class="demo1">
        <h4 class="demo">姓名:{{name}}</h4>
        <h4>年龄:{{sex}}</h4>   
    </div>
</template>
<script>
//组件的交互，数据和方法
export default {
    name:'Student',
     data() {
        return{
            name:'张三',
            sex:'女',
        };
     },
    
    };
</script>

<style scoped>
/*组件的样式*/
.demo1{
background-color: rgb(4,243,5);
}
</style>