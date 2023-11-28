<script lang="ts">
  import Button from "./components/Button.svelte";
  import Description from "./components/Description.svelte";
  import { mgid } from "megaid"

  let id: string = mgid()

  const generateId = () => {
    id = mgid()
  }
  
</script>

<main>
  <div id="container">
    <p>mega-id</p>
    <input bind:value={id} />
    <Button generateId={generateId} />
    <Description />
  </div>
</main>

<style>

#container {
  display: flex;
  flex-direction: column;
  gap: 20px;
}

input {
  padding-right: 20px;
  padding-left: 5px;
  padding-top: 10px;
  padding-bottom: 10px;
  border-radius: 7px;
  border: none;
}

</style>










