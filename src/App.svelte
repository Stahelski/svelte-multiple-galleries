<script>
  import Gallery from "./Gallery.svelte";
  import Gallery2 from "./Gallery2.svelte";

  let activeGallery = null;
  let showMenu = false;

  function toggleGallery(galleryName) {
    if (activeGallery === galleryName) {
      activeGallery = null;
    } else {
      activeGallery = galleryName;
    }
    showMenu = false;
  }

  function toggleMenu() {
    showMenu = !showMenu;
  }
</script>

<main>
  <div class="min-container">
    <h1>My gallery page</h1>
  </div>

  <div class="menu-container">
    <button class="menu-button" on:click={toggleMenu}>
      {showMenu ? "Close Menu" : "Open Menu"}
    </button>
    {#if showMenu}
      <div class="menu-content">
        <button on:click={() => toggleGallery("ronin")}>
          {activeGallery === "ronin" ? "Remove Ronin" : "Add Ronin"}
        </button>

        <button on:click={() => toggleGallery("landscape")}>
          {activeGallery === "landsape" ? "Remove Landscape" : "Add Landscape"}
        </button>
      </div>
    {/if}
  </div>

  {#if activeGallery === "ronin"}
    <Gallery />
  {/if}

  {#if activeGallery === "landscape"}
    <Gallery2 />
  {/if}
</main>

<style>
  :root {
    background-color: rgb(32, 32, 32);
  }

  h1 {
    color: #b80000;
  }

  button {
    font-size: 1em;
    padding: 10px 20px;
    margin: 20px 0;
    background-color: #4caf50;
    color: white;
    border: none;
    border-radius: 4px;
    cursor: pointer;
  }

  button:hover {
    background-color: #45a049;
  }
</style>
