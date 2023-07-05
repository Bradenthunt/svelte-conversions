<script>
  import TempControl from "./TempControl.svelte";
</script>

<div>
  <p>Car Menu</p>
  <TempControl />
  <div>
    <p>My Apps</p>
  </div>
  <div>
    <p>Recent Apps</p>
  </div>
  <TempControl />
  <p>Volume Control</p>
</div>

<style>
  div {
    width: 100vw;
    display: flex;
    justify-content: space-evenly;
    align-items: center;
    gap: 20px;
    background-color: black;
    color: white;
    padding: 10px;
  }
</style>
