<script>
  import marioFont from "./assets/mariofont.png";
  import goomba from "./assets/goomba-removebg-preview.png";
  import bobombs from "./assets/Bob-omb-removebg-preview.png";
  import cheepcheeps from "./assets/Cheep_Cheep-removebg-preview.png";

  let goombaTotal;
  let bobombsTotal;
  let cheepsTotal;

  function pestControlTotal(event) {
    let totalCost = goombaTotal * 5 + bobombsTotal * 7 + cheepsTotal * 11;

    document.getElementById(
      "total"
    ).textContent = `The total cost for your requested services will be ${totalCost} coins.`;
  }
</script>

<main>
  <img id="mario-pest-control" src={marioFont} alt="mario font" />

  <form name="pest-cost" on:submit|preventDefault={pestControlTotal}>
    <div class="baddie-card">
      <label for="goomba">Goombas: 5 Coins</label>
      <img class="baddie" src={goomba} alt="goomba" />
      <input
        type="number"
        id="goomba"
        placeholder="~ Number of Pest ~"
        bind:value={goombaTotal}
      />
    </div>
    <div class="baddie-card">
      <label for="bobomb">Bob-ombs: 7 Coins</label>
      <img class="baddie" src={bobombs} alt="bobomb" />
      <input
        type="number"
        id="bobomb"
        placeholder="~ Number of Pest ~"
        bind:value={bobombsTotal}
      />
    </div>
    <div class="baddie-card">
      <label for="cheepcheep">Cheep-cheeps: 11 Coins</label>
      <img class="baddie" src={cheepcheeps} alt="cheepcheep" />
      <input
        type="number"
        id="cheepcheep"
        placeholder="~ Number of Pest ~"
        bind:value={cheepsTotal}
      />
    </div>
    <button>Submit</button>
  </form>
  <div id="total" />

  <div id="footer">
    <p>mario@mariopestcontrol.com</p>
    <p>mariopestcontrol.com</p>
    <p>Somewhere in the Mushroom Kingdom</p>
  </div>
</main>

<style>
  #mario-pest-control {
    margin-bottom: 20px;
  }

  .baddie {
    width: 200px;
    height: 200px;
  }

  .baddie-card {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    margin-bottom: 20px;
    gap: 10px;
  }

  #footer {
    display: flex;
    justify-content: space-between;
  }
</style>
