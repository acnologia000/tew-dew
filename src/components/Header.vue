<template>
    <header>
        <h1>{{title}}</h1>
        <Button BtnLable="Add item" color="green"/>
    </header>
</template>

<script>
import Button from "./button.vue"
export default {
    name:"Header", // name of the exported component
    props:{
        title:{ // prop name
            type:String, // prop type
            default:"Some default header string" // prop default value
        }
    },
    components:{
        Button, // register imported component to use  
    },
}
</script>

<style scoped>
    header{
        display: flex;
        justify-content: space-around;
        align-items: center;
    }
</style>