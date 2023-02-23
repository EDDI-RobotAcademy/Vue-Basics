<template>
  <v-container>
    <table-component :table-data="tableData"/>
  </v-container>
</template>

<script>

import TableComponent from '@/components/lecture/emitTest/TableComponent.vue'

// 오목 게임
// 바둑판, 승자 판정 그 다음 아직 모르겠음.

export default {
    name: "EmitTestBoardGame",
    components: {
        TableComponent
    },
    data () {
        return {
            // tableData[5][5]
            tableData: [
                ['', '', '', '', ''],
                ['', '', '', '', ''],
                ['', '', '', '', ''],
                ['', '', '', '', ''],
                ['', '', '', '', ''],
            ]
        }
    }
}

</script>

<style>

</style>