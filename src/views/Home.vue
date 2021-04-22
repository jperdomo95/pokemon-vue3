<template>
  <div>
    <h1 class="text-5xl text-center mb-4">Home</h1>
    <PokemonsListComponent :pokemons="pokemons" />
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import PokemonsListComponent from '@/components/pokemons/PokemonsList.component.vue'

export default defineComponent({
  name: 'Home',
  components: {
    PokemonsListComponent
  },
  setup () {
    const pokemons: any[] = [
      {
        id: 1,
        name: 'Bulbasaur',
        image: 'https://raw.githubusercontent.com/PokeAPI/sprites/master/sprites/pokemon/1.png'
      },
      {
        id: 2,
        name: 'ivysaur',
        image: 'https://raw.githubusercontent.com/PokeAPI/sprites/master/sprites/pokemon/2.png'
      },
      {
        id: 3,
        name: 'venusaur',
        image: 'https://raw.githubusercontent.com/PokeAPI/sprites/master/sprites/pokemon/3.png'
      }
    ]
    return {
      pokemons
    }
  }
})
</script>
