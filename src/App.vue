<template>
  <div id="app">
    <div id="form_main" class="content-header">
      <div class="logo">
        <img src="./assets/pokemon_logo.png" alt="Logo Pokemón" />
      </div>

      <div class="searchPokemon" for="form__principal">
        <input
          type="text"
          id="form__principal"
          placeholder="Ingresa nombre de Pokemón"
          v-model="nombre"
        />

        <button @click="pokebusca" class="button-search">
          <div class="button-content">
            Buscar
            <img src="./assets/pokebola.png" alt="Pokebola en botón" />
          </div>
        </button>
      </div>
    </div>

    <section class="pokemonRespuesta">
      <h2>Movimientos</h2>
      <h2>Habilidades</h2>
    </section>
  </div>
</template>

<script>
import axios from "axios";
export default {
  name: "App",
  data() {
    return {
      nombre: "pikachu",
    };
  },
  methods: {
    pokebusca() {
      if (this.nombre) {
        axios
          .get(`https://pokeapi.co/api/v2/pokemon/${this.nombre}`)
          .then((response) => {
            console.info(response.data);
          })
          .catch((error) => {
            console.log(error);
            alert("El nombre no existe");
          });
      } else {
        alert("El pokémon no existe, ingresa otro nombre");
      }
    },
  },
};
</script>
<style src="./assets/style.css"></style>
