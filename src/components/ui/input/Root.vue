<script setup lang="ts">
import { computed, useAttrs } from "vue";

interface Props {
  isError?: boolean;
}

const props = defineProps<Props>();

const attrs = useAttrs();

const classes = computed(() => [
  "container",
  {
    "container--error": props.isError,
  },
  attrs.class,
]);
</script>

<template>
  <div
    v-bind="attrs"
    :data-error="props.isError"
    :class="classes"
    class="containerInput"
  >
    <slot />
  </div>
</template>

<style scoped>
.containerInput {
  display: flex;
  align-items: center;
  border-radius: 0.5rem;
  /* gap: 0.5rem; */
  /* padding: 0.75rem; */
  background-color: #fff;
  border: none;
  /* border-radius: 4px; */
  padding: 0.5rem 0.5rem;
  gap: 0.5rem;
}

.container {
  width: 100%;
}

.container--error {
  border-color: red;
}
</style>
