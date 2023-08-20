<template>
    <div>
        <form @submit.prevent="createPost">
            <label for="userId">Post User Id</label>
            <input type="text" id="userId" v-model="formData.userId"><br>
            <label for="title">Post Title</label>
            <input type="text" id="title" v-model="formData.title"><br>
            <label for="body">Post Body</label>
            <input type="text" id="body" v-model="formData.body">br

            
            <button>CreatePost</button>
            {{ formData }}
        </form>
        {{ }}
    </div>
</template>

<script>
    import axios from 'axios';
    export default {
        name:'CreatePost',
        data(){
            return{
                formData:{
                    userId:'',
                    title:'',
                    body:''
                }
            }
        },
        methods:{
            createPost(){
                axios.post('https://jsonplaceholder.typicode.com/posts',this.formData)
                .then(r=>console.log(r))
                .catch(e=>console.log(e))
            }
        }
    }
</script>

<style lang="scss" scoped>

</style>