<template>
 <div>
    <h1>{{msg}}</h1>
        <h4>姓名:{{studentName}}</h4>
        <h4>年龄:{{age}}</h4>   
         <h4>年龄:{{age +1}}</h4>   
    </div>
</template>
<script>
//组件的交互，数据和方法
export default {
    name:'Student',
     data() {
        return{
            msg:'我是一名学生',
        };
     },
    //  props:['studentName','age'],
    // props:{
    //     studentName:String,
    //     age:Number,
    // },
    props:{
        studentName:{
          type:String,
        },
       age:{
          type:Number,
        //   required:true
        },
    },
    //  methods:{
    //     show(){
    //         console.log('@@@');
    //     }
    //  }
    };
</script>

<style>
/*组件的样式*/

</style>