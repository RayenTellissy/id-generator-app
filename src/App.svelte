<script lang="ts">
  import { mgid } from "megaid"

  let id: string = mgid()
  let length: number | null = null

  const generateId = () => {
    id = mgid()
  }
  
</script>

<main>
  <div id="container">
    <p>mega-id</p>
    <input bind:value={id} />
    <button on:click={generateId}>generate id</button>
    <p id="description">this can be used as a password, tagname, IDs for a database and many other things...</p>
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

#description {
  opacity: 30%;
  user-select: none;
  transition: opacity 300ms ease-in-out;
}

#description:hover {
  opacity: 100%;
}

</style>
