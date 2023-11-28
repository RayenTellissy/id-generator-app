<script lang="ts">
  import { mgid } from "megaid"

  export let generateId: () => void

</script>

<button on:click={() => generateId()}>generate id</button>

<style>

</style>
