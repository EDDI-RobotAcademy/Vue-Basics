<template>
  <td @click="whichOneSelected" style="width: 30px; height: 30px">
    {{ cellData }}
  </td>
</template>

<script>

export default {
    name: "TdComponent",
    data () {
        return {

        }
    },
    props: {
        cellData: String,
        cellIndex: Number,
        rowIndex: Number,
        tableData: Array,
        currentTurnShape: String,
    },
    methods: {
        whichOneSelected () {
            console.log('오목판을 클릭했습니다!')

            this.$set(this.tableData[this.rowIndex], this.cellIndex, this.currentTurnShape)
        }
    }
}

</script>

<style>

</style>