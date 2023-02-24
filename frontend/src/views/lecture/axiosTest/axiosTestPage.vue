<template>
  <v-container>
    <form @submit.prevent="onSubmit">
      <table>
        <tr>
          <td>이름</td>
          <td>
            <input type="text" v-model="memberName"/>
          </td>
        </tr>

        <tr>
          <td>전공</td>
          <td>
            <input type="text" v-model="major"/>
          </td>
        </tr>
      </table>

      <div>
        <button type="submit">전송</button>
      </div>
    </form>
  </v-container>
</template>

<script>
export default {

}
</script>

<style>

</style>