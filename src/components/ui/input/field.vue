<script setup lang="ts">
import { useAttrs } from "vue";

const attrs = useAttrs();
</script>

<template>
  <input v-bind="attrs" class="input" />
</template>

<style scoped>
.input {
  width: 100%;
  /* height: 100%; */
  height: 2.5rem;

  padding: 1rem;

  border-radius: 0.2rem;

  background: transparent;
  /* border: 1px solid #222; */
  border: 1px solid var(--color-text-secondary);
  color: white;
}

/* .input::placeholder {
  color: var(--color-placeholder);
} */
</style>
