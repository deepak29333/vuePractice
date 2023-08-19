<template>
  <!-- <Greet name="Deepak" hero-name="supetMan" />
  <Greet name="Bruce"  hero-name="batman" />
  <Greet  name="Ankit" hero-name="spiderman" />
  <Greet  :name="name" :hero-name="channel" /> -->
    <!-- <Article id="my-article" title="Article Title" 
    :likes="10" :isPublished="true" /> -->\
    <h2> App component username:{{ name }}</h2>
      <ComponentC/>
      <button @click="showPopup=true" >show Popup</button>
      <Popup v-show="showPopup" @close="closePopup" />
 </template>

<script>
import ComponentC from './components/ComponentC.vue';
import Popup from './components/Popup.vue';

// import Greet from "./components/Greet.vue";
// import Article from "./components/Article.vue";

export default {
  name: 'App',
  components:{
    ComponentC,
    Popup
},
 data(){
  return{
    name:'deepak',
    showPopup:false
  }
},
methods:{
  closePopup(name){
    this.showPopup=false,
    console.log('name',name)
  }
},
  provide(){
    return{
      username:this.name
    }
      
    }

}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
