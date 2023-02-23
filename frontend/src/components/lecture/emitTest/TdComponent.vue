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
            game: {
                propsTurnShape: this.currentTurnShape,
            }
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

            this.$emit('callTest');
            this.changeTurn()
            this.$emit('updateTurnShape', this.game.propsTurnShape)
        },
        changeTurn () {
            this.game.propsTurnShape = this.currentTurnShape === 'O' ? 'X' : 'O'
        }
    }
}

</script>

<style>

</style>