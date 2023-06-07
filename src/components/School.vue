<template>
 <div class="demo">
        <h4>学校:{{schoolname}}</h4>
        <h4>地址:{{address}}</h4>   
    </div>
</template>
<script>
//组件的交互，数据和方法
export default {
    name:'School',
     data() {
        return{
            schoolname:'山东商务',
            address:'烟台',
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
.demo{
    background-color: yellow;
}
</style>