<template>
    <div>
        <button @mouseover="incrementCount" > clicked {{ count }} times</button>
    </div>
</template>

<script>
import CounterMixin from '../mixins/counter';

    export default {
        name:'HoverCounter',
       mixins:[CounterMixin]
    }
</script>

<style lang="scss" scoped>

</style>