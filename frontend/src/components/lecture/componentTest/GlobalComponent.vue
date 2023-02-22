<template>
    <button @click="addCounter">{{ counterValue }}</button>
</template>

<script>

export default {
    name: "GlobalComponent",
    props: ['initialTest'],
    data () {
        return {
            counterValue: this.initialTest
        }
    },
    methods: {
        addCounter () {
            this.counterValue += 1
        }
    }
}

</script>

<style>

</style>