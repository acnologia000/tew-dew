<template>
    
    // eslint-disable-next-line vue/require-v-for-key
    <div v-for="task in tasks" :key="task">
        <h1>{{task.text}}</h1>
    </div>
</template>


<script>
export default {
    name:"Tasks",
    setup() {
        
    },
    props:{
        tasks:Array
    }
}
</script>