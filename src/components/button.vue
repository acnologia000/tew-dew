<template>
    <button @click="add()" v-bind:style="{background:color}" class="btn">{{BtnLable}}</button>
</template>


<style scoped>

</style>

<script>
export default {
    name:"Button",
    setup() {
        
    },
    props:{
        BtnLable:{
            type:String,
            default:"Button"
        },
        color:{
            type:String,
            default:"green"
        },
        
    },

    methods:{
        add(){
            console.log("click")
        },
    }


}
</script>