<template>
    <div class="card" >
        <slot name="header"></slot>
        <slot></slot>
        <slot name="footer"></slot>
    </div>
</template>

<script>
    export default {
        name:'Card'
    }
</script>

<style lang="scss" scoped>

</style>