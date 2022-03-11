<script>
  import { onMount } from "svelte";

  let images = [];

  onMount(async () => {
    console.log("onMount");
    const respuesta = await fetch("https://rickandmortyapi.com/api/character");

    const data = await respuesta.json();

    images = data.results;
  });
</script>

<style>
  section {
    display: grid;
    grid-template-columns: repeat(5, 1fr);
    gap: 3rem;
    padding: 2.5rem;
  }

  figure {
    margin: 0;
    text-align: center;
  }

  img {
    width: 100%;
  }
</style>

<div class="PhotosComponent">
  <section>
    {#each images as character}
      <figure>
        <img src={character.image} alt={character.name} />
        <figcaption>{character.name}</figcaption>
      </figure>
    {:else}
      <p>Loading</p>
    {/each}
  </section>
</div>
