<script>
  import Cell from './Cell.svelte'
  export let cols
  export let row
  export let rowData 
  export let handleChangedCell
</script>

<style>
.row {
  display: block;
}
</style>

<div class="row">
{#each Array(cols) as _, col}
  <Cell
    row={row}
    col={col}
    value={rowData[col] || ''}
    onChangedValue={handleChangedCell}
  />
{/each}
</div>