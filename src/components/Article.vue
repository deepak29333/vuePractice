<template>
    <div>
        hi i am article component
        {{ title }} {{likes }}
        <h2 v-bind="$attrs" >isPublished -{{isPublished? 'yes':'no' }}</h2>
    </div>
</template>

<script>
    export default {
        name:'Article',
        props:{
            title:{
                type:String,
                required:true,
                dafault:'Artical Default Title'
            },
            likes:Number,
            isPublished:Boolean
        },
        inheritAttrs:false
    }
   
</script>

<style scoped>

</style>