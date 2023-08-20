<template>
  <div>
     <Card>this is card</Card>
     <Card></Card>
     <Card> <h2> this is card2 </h2> </Card>
     <Card> <img src="https://picsum.photos/200" alt=""> </Card>
     <Card> 
      <template v-slot:header >
        <div>
          this is header slot
        </div>
      </template>
     </Card>
     <Card> 
      <template v-slot:default >
        <div>
          <img src="https://picsum.photos/200" alt="">
        </div>
      </template>
     </Card>
     <Card> 
      <template v-slot:footer >
        <div>
          <button>vue details</button>
        </div>
      </template>
     </Card>

     <NameList>
        <template v-slot:default="slotProps" >
         {{slotProps.firstName}}{{ slotProps.lastName }}
        </template>
     </NameList>

     <NameList>
        <template v-slot:default="slotProps" >
         {{slotProps.lastName}}{{ slotProps.firstName }}
        </template>
     </NameList>
     <NameList>
        <template v-slot:default="slotProps" >
        {{ slotProps.firstName }}
        </template>
     </NameList>
  </div>
 </template>

<script>
import Card from './components/Card.vue';
import NameList from './components/NameList.vue';
export default {
  name: 'App',
  components:{
    Card,
    NameList
},
 data(){
  return{
    name:''
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
