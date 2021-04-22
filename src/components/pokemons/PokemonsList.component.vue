<template>
  <h1 class="text-lg text-center">Pokemons</h1>
</template>

<script lang="ts">
import { defineComponent, PropType } from 'vue'

export default defineComponent({
  props: {
    items: {
      type: Array as PropType<any[]>
    }
  }
})
</script>

<style>

</style>
