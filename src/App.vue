<template>
  <div id="app">
    <form id="form_main" class="content-header">
      <div class="logo">
        <img src="./assets/pokemon_logo.png" alt="Logo Pokemón" />
      </div>

      <div class="searchPokemon" for="form__principal">
        <input type="text" id="form__principal" placeholder="Ingresa nombre de Pokemón" />

        <button class="button-search">
          <div class="button-content">
            Buscar
            <img src="./assets/pokebola.png" alt="Pokebola en botón" />
          </div>
        </button>
      </div>
    </form>

    <section class="pokemonRespuesta"></section>
  </div>
</template>

<script>
// import HelloWorld from "./components/HelloWorld.vue";

export default {
  name: "App"
  // components: {
  //   HelloWorld
  // }
};
</script>

<style src="./assets/style.css">
#app {
}
</style>
