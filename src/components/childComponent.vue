<template>
 <div>
        <input type="text"
        v-model="myMessage"
        @input="passData(myMessage)">
    </div>
</template>
<script>
export default {
    name:'childComponet',
     data() {
        return{
           myMessage:this.message,
        };
     },
    props:{
        message:String,
    },
    methods:{
        passData(val){
            this.$emit('getChildData',this.myMessage)
        },
    },
    };
</script>

<style scoped>

</style>