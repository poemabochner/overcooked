<script lang="ts">
import SelecionarIngredientes from './SelecionarIngredientes.vue';
import SuaLista from './SuaLista.vue';

export default {
  data() {
    return {
      ingredientes: [] as string[]
    }
  },
  components: { SelecionarIngredientes, SuaLista },

  methods: {
    adicionarIngrediente(ingrediente: string) {
      this.ingredientes.push(ingrediente)
    },
    removerIngrediente(ingrediente: string) {
      this.ingredientes = this.ingredientes.filter(iLista => ingrediente !== iLista);
    },
  }
}
</script>

<template>
  <main class="conteudo-principal">
    <SuaLista :ingredientes="ingredientes" />

    <SelecionarIngredientes @adicionar-ingrediente="adicionarIngrediente" @remover-ingrediente="removerIngrediente" />
  </main>
</template>
