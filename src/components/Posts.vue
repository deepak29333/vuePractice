<template>
    <div>
        <!-- <button @click="getPosts" >Load post</button> -->
        <div v-for="post of posts" :key="post.id" >
        <h3>{{ post.id }}. {{ post.title }}</h3>
        <p>{{ post.body }}</p>
        <hr>
        </div>
        <h3 v-if="errorMgs">{{errorMgs }}</h3>
        <input type="text" ref="inputRef" />
    </div>
</template>

<script>
import axios from 'axios'
    export default {
        name:'Posts',
        mounted(){
            this.$refs.inputRef.focus();
        },
        created(){
            // this.$refs.inputRef.focus();
            this.getPosts();
        },
        data(){
            return{
                posts:[],
                errorMgs:''
            }
        },
        methods:{
            getPosts(){
                axios.get('https://jsonplaceholder.typicode.com/posts')
                .then((response)=>{
                    this.posts=response.data,
                    console.log(response.data);
                })
                .catch(e=>{
                    this.errorMgs='Api Retriving Data'
                    console.log(e);
                })
            }
        }
    }
</script>

<style lang="scss" scoped>

</style>