<template>
    <div>
        <h2>component C</h2>
        <ComponentE/>
    </div>
</template>

<script>
import ComponentE from './ComponentE.vue';

    export default {
    name: 'ComponentC',
    components: { ComponentE }
}
</script>

<style lang="scss" scoped>

</style>