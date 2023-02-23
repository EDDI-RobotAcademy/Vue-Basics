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

            this.setDataToSelectedArray()

            this.changeTurn()
            
        },
        changeTurn () {
            this.game.propsTurnShape = this.currentTurnShape === 'O' ? 'X' : 'O'
            // this.$emit('이벤트명', 값(옵션))
            this.$emit('updateTurnShape', this.game.propsTurnShape)
        },
        setDataToSelectedArray () {
            // this.tableData[this.rowIndex]: 사용자가 클릭한 행 정보
            // this.cellIndex: 사용자가 클릭한 '행'내 열 정보
            // this.currentTurnShape: 현재 턴('x', 'o')
            // this.$set(행, 열, 값) -> 특정[행][열] = 값
            this.$set(this.tableData[this.rowIndex], this.cellIndex, this.currentTurnShape)
        }
    }
}

</script>

<style>

</style>