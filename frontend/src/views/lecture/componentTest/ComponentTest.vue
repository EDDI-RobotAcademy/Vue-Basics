<template>
  <v-container>
    <!--
        public void global-component (Long initial-test) {
            blablabla ~~~~
        }

        global-component(counter);
    -->
    <global-component :initial-test="counter" :increment-value="incValue1"/><br/>
    <global-component :initial-test="start" :increment-value="incValue2"/><br/>
  </v-container>
</template>

<script>

export default {
    name: "ComponentTest",
    data () {
        return {
            counter: 0,
            start: 100,
            incValue1: 1,
            incValue2: 2,
        }
    }
}

</script>

<style>

</style>