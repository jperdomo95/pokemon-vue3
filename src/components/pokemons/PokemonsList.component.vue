<template>
  <div class="container mx-2 md:mx-auto">
    <h1 class="text-3xl mb-4 text-center">Wild Pokemon</h1>
    <div class="grid gap-5 md:gap-10  grid-cols-1 md:grid-cols-3">
      <div v-for="pokemon in pokemons" :key="pokemon.id" class="flex flex-col items-center px-5 shadow-lg rounded-lg border-2 pb-5">
        <img :src="pokemon.image" :alt="pokemon.name" class="w-40">
        <p class="text-center text-xl mb-5">{{ pokemon.name }}</p>
        <button class="p-2 bg-blue-500 rounded-lg text-white font-bold">CATCH!</button>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent, PropType } from 'vue'
import { PokemonInterface } from '@/models/pokemons/Pokemon.interface'

export default defineComponent({
  props: {
    pokemons: {
      type: Array as PropType<PokemonInterface[]>
    }
  }
})
</script>

<style>

</style>
