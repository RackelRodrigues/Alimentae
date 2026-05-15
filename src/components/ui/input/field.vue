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
  height: 54px;

  padding-inline: 1rem;

  border-radius: 14px;

  background: #111;
  border: 1px solid #222;

  color: white;
}
</style>
