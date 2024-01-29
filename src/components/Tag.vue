<template>
  <span class="tag">
    {{ texto }}
  </span>
</template>

<script lang="ts">
  export default {
    props: {
      texto: {
        type: String, required: true
      }
    }
  }
</script>

<style scoped>
  .tag {
  display: inline-block;
  border-radius: 0.5rem;
  min-width: 4.25rem;
  padding: 0.5rem;
  text-align: center;
  transition: 0.2s;
  color: var(--creme, #FFFAF3);
  background: var(--pink);
  font-weight: 700;
}
</style>