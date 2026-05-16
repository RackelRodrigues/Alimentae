<script setup lang="ts">
import { computed, useAttrs } from "vue";

interface Props {
  variant?: "default" | "primary" | "secondary" | "terciary";
}

const props = withDefaults(defineProps<Props>(), {
  variant: "default",
});

const attrs = useAttrs();

const classes = computed(() => [
  "button",
  `button-${props.variant}`,
  attrs.class,
]);
</script>

<template>
  <button v-bind="attrs" :class="classes">
    <slot />
  </button>
</template>

<style lang="css" scoped>
.button-primary {
  background-color: transparent;
  border: 1px solid var(--color-accent);
  color: var(--color-accent);
  border-radius: 0.25rem;
  display: flex;
  align-items: center;
  gap: 0.2rem;
  padding: 0.2rem 0.4rem;
  cursor: pointer;
  font-size: 0.9rem;
}

.button-secondary {
  background-color: var(--color-primary);
  color: white;
  border: none;
  border-radius: 0.25rem;
  display: flex;
  align-items: center;
  gap: 0.2rem;
  padding: 0.3rem 0.8rem;
  cursor: pointer;
}

.button-terciary {
  background-color: var(--color-accent);
  color: var(--color-white);
  border: none;
  display: flex;
  align-items: center;
  gap: 0.2rem;
  padding: 0.3rem 0.8rem;
  border-radius: 0.3rem;
  cursor: pointer;
  font-size: 0.9rem;
}

.button-primary:hover {
  background-color: var(--color-accent-hover);
  filter: brightness(0.9);
  color: white;
}

.button-secondary:hover {
  background-color: var(--color-primary-hover);
}

.button-terciary:hover {
  background-color: var(--color-accent-hover);
}
</style>
