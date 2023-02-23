<template>
  <v-container>
    <table-component 
        :table-data="tableData"
        :current-turn-shape="currentTurnShape"
        @updateTurnShape="updateTurnShape"/>
  </v-container>
</template>

<script>

import TableComponent from '@/components/lecture/emitTest/TableComponent.vue'

// 오목 게임
// 바둑판, 승자 판정 그 다음 아직 모르겠음.
// 누구 차례인지 어떻게 알지 ?
// 'O', 'X' 표시로 순서를 구분하자!

export default {
    name: "EmitTestBoardGame",
    components: {
        TableComponent
    },
    data () {
        return {
            currentTurnShape: 'O',
            // tableData[5][5]
            tableData: [
                ['', '', '', '', ''],
                ['', '', '', '', ''],
                ['', '', '', '', ''],
                ['', '', '', '', ''],
                ['', '', '', '', ''],
            ]
        }
    },
    methods: {
        updateTurnShape (receivedTurnShape) {
            console.log('Board Game received Table Component info: ' + receivedTurnShape)

            this.currentTurnShape = receivedTurnShape;
        }
    }
}

</script>

<style>

</style>