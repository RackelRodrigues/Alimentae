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
  `button--${props.variant}`,
  attrs.class,
]);
</script>

<template>
  <button v-bind="attrs" :class="classes">
    <slot />
  </button>
</template>

<style lang="css" scoped></style>
