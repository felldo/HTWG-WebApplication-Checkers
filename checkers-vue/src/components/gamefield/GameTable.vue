<template>
  <table id="gameTable" class="tableAlignment">
    <tr v-for="(row, indexRow) in field.rows" :key="row.id">
      <Cell v-for="(cell, indexColumn) in row" :indexRow=indexRow :indexColumn=indexColumn :cellValue=cell
            :key="cell.id"></Cell>
    </tr>
  </table>
</template>


<script>
import Cell from "@/components/gamefield/Cell";
export default {
  name: 'GameTable',
  components: {
    Cell,
  },
  props: ['field']
};

</script>

<style>
.tableAlignment {
  margin-left: auto;
  margin-right: auto;
  border-collapse: separate !important;
  border-spacing: 0px !important;
}
</style>