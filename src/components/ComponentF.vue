<template>
    <div>
        <h2>component F</h2>
        <h3> componet f  username {{username}}</h3>
    </div>
</template>

<script>
    export default {
        name:'ComponentF',
        inject:['username']
    }
</script>

<style lang="scss" scoped>

</style>