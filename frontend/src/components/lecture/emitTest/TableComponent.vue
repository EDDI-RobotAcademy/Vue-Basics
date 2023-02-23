<template>
  <table>
    <!-- tableData -> arr[4][4]
         rowData   -> arr[0] ~ arr[4]
         arr[0]    -> arr[0][0] ~ arr[0][4]
          ...      ->          ...
         arr[4]    -> arr[4][0] ~ arr[4][4]
         index     -> 0 ~ 4           -->
    <tr-component
        v-for="(rowData, index) in tableData" :key="index"
        :row-data="rowData"
        :row-index="index"
        :tableData="tableData"
        :current-turn-shape="currentTurnShape"
        @updateTurnShape="updateTurnShape"/>
  </table>
</template>

<script>

import TrComponent from '@/components/lecture/emitTest/TrComponent.vue'

export default {
    name: "TableComponent",
    components: {
        TrComponent
    },
    props: {
        tableData: Array,
        currentTurnShape: String,
    },
    method: {
        updateTurnShape (receivedTurnShape) {
            console.log('Table Component received Tr Component info: ' + receivedTurnShape)

            this.turnShape = receivedTurnShape;
            this.$emit('updateTurnShape', this.turnShape)
        }
    }
}

</script>

<style>

</style>