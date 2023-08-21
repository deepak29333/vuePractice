<template>
  <h2> this is main component</h2>
  <!-- <ChildStyle/> -->
  <!-- <Posts/>
  <CreatePostVue/> -->
  <ClickCounter/>
  <HoverCounter/>
 </template>

<script> 
// import Posts from './components/Posts.vue';
// import CreatePostVue from './components/CreatePost.vue'; -->
// import ChildStyle from './components/ChildStyle.vue';
import ClickCounter from './components/ClickCounter.vue';
import HoverCounter from './components/HoverCounter.vue'
export default {
  name: 'App',
  components:{
    // Posts,
    // CreatePostVue,
    ClickCounter,
    HoverCounter
},
 data(){
  return{
    name:''
  } 
}

}
</script>

<style >
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
h2{
  color: orange;
}
</style>
