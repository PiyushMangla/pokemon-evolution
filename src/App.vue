<template>
  <pokemonCards :pokemons="pokemons" @evolve="evolveState" />
  <pokemonCards :pokemons="pokemonEvolve" />
</template>

<script>
import PokemonCards from "./components/pokemonCards.vue";
import { pokemonCompose } from "./components/pokemonApi.js";
export default {
  name: "App",
  components: { PokemonCards },
  setup() {
    const { pokemons, evolveState, pokemonEvolve } = pokemonCompose();

    return { pokemons, evolveState, pokemonEvolve };
  },
};
</script>

<style >
</style>