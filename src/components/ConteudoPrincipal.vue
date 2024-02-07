<script lang="ts">
import SelecionarIngredientes from './SelecionarIngredientes.vue';
import SuaLista from './SuaLista.vue';

export default {
  data() {
    return {
      ingredientes: ['Alho', 'Manteiga', 'Orégano']
    }
  },
  components: { SelecionarIngredientes, SuaLista }
}
</script>

<template>
  <main class="conteudo-principal">
    <SuaLista :ingredientes="ingredientes" />

    <SelecionarIngredientes />
  </main>
</template>
