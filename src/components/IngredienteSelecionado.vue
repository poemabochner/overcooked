<template>
  <button class="ingrediente" @click="aoClicar()" :aria-pressed="selecionado">
    <Tag :texto="ingrediente" :ativa="selecionado"></Tag>
  </button>
</template>

<script lang="ts">
import Tag from './Tag.vue';

  export default {
    components: {Tag},
    props: {
      ingrediente: {
        type: String, required: true
      }
    },
    data () {
    return {
      selecionado: false
    }
  },

  methods: {
    aoClicar() {
      this.selecionado = !this.selecionado

      if (this.selecionado) {
        this.$emit('adcionarIngrediente', this.ingrediente)
      }
    }
  }
  }
</script>

<style scoped>
.ingrediente {
    cursor: pointer;
}
</style>