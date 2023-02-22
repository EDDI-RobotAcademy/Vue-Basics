<template>
  <v-container>
    <global-component :initial-test="counter"/>
  </v-container>
</template>

<script>

export default {
    name: "ComponentTest",
    data () {
        return {
            counter: 0,
        }
    }
}

</script>

<style>

</style>