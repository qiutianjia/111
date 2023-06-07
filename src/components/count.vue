<template>
    <div class="count">
        <span class="reduce" @click="reduce"></span>
        <input type="number" v-model="num" @change="change">
        <span class="plus" @click="plus"></span>
    </div>
</template>
 
<script>
    export default {
        name: "count",
        data(){
            return {
                num:'0'
            }
        },
        props:{
            value:{
                type:Number,
                default:0
            },
            max:{
                type:Number,
                default:10
            }
        },
        created(){
            this.inspect();
        },
        methods:{
            reduce(){
                     if(this.num>1){
                    this.num--;
                    this.$emit('input', this.num);
                }else{
                    alert('不能小于1')
                }
              
            },
            plus(){
                if(this.num<this.max){
                    this.num++;
                    this.$emit('input', this.num);
                }else{
                    alert('不能大于10')
                }
            },
            change(){
                
            },
            
        },
        watch: {
            value(newVal) {
                this.num = newVal
            }
        }
    }
</script>
 
<style scoped>
    .count span{
        display: inline-block;
        position: relative;
        overflow: hidden;
        box-sizing: border-box;
        width: 30px;
        height: 30px;
        color:red;
        vertical-align: middle;
        background: #ebedf0;
        border-radius: 2px;
        border: 1px solid black;
    }
    .count span:after{
        content: '';
        position: absolute;
        top: calc((100% - 2px) / 2);
        left: 25%;
        background-color: #c9c9c9;
        width: 50%;
        height: 2px;
    }
    .count .plus:before{
        content: '';
        width: 2px;
        height: 50%;
        position: absolute;
        left: calc((100% - 2px) / 2);
        top: 25%;
        background-color: #c9c9c9;
    }
    .count input{
        display: inline-block;
        width: 40px;
        height: 30px;
        border: none;
        box-sizing: border-box;
        vertical-align: middle;
        text-align: center;
        margin: 0 1px;
         border: 1px solid black;
        font-size: 13px;
    }
</style>