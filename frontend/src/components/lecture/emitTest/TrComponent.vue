<template>
  <tr>
    <!-- arr[rowIndex][index]

         rowData    -> arr[0]    ~ arr[4]
         rowData[0] -> arr[0][0] ~ arr[0][4] -> cellData
          ...       ->          ...          -> cellData
         arr[4]     -> arr[4][0] ~ arr[4][4] -> cellData
    -->
    <td-component
        v-for="(cellData, index) in rowData" :key="index"
        :cell-data="cellData"
        :cell-index="index"
        :row-index="rowIndex"
        :table-data="tableData"/>
  </tr>
</template>

<script>

import TdComponent from '@/components/lecture/emitTest/TdComponent.vue'

export default {
    name: "TrComponent",
    components: {
        TdComponent
    },
    props: {
        rowData: Array,
        rowIndex: Number,
        tableData: Array,
    }
}
</script>

<style>

</style>