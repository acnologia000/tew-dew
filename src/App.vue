<template>
  <Header title = "Maurice pork Shop"/>
   <Tasks :tasks="tasks"/> <!-- tasks variabe from data() on line 17 -->
</template>

<script>
import Header from "./components/Header.vue"
import Tasks from "./components/tasks.vue"


export default {
  name: 'App',
  components: {
    Header,
    Tasks,
  },
  data(){
    return{
      tasks:[
        {id:1,text:"some title text1",day:"1/1/21",reminder:false},
        {id:2,text:"some title text2",day:"1/1/22",reminder:true},
        {id:3,text:"some title text3",day:"1/1/23",reminder:false},
        {id:4,text:"some title text4",day:"1/1/24",reminder:true},
      ]
    }
  },
  created(){// lifecycle method to load data on component creation
      console.log("app.vue created")
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;400&display=swap');
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}
body {
  font-family: 'Poppins', sans-serif;
}
.container {
  max-width: 500px;
  margin: 30px auto;
  overflow: auto;
  min-height: 300px;
  border: 1px solid steelblue;
  padding: 30px;
  border-radius: 5px;
}
.btn {
  display: inline-block;
  background: #000;
  color: #fff;
  border: none;
  padding: 10px 20px;
  margin: 5px;
  border-radius: 5px;
  cursor: pointer;
  text-decoration: none;
  font-size: 15px;
  font-family: inherit;
}
.btn:focus {
  outline: none;
}
.btn:active {
  transform: scale(0.98);
}
.btn-block {
  display: block;
  width: 100%;
}
</style>
