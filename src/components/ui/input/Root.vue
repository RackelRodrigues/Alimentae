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
  <div v-bind="attrs" :data-error="props.isError" :class="classes">
    <slot />
  </div>
</template>

<style scoped>
.container {
  width: 100%;
}

.container--error {
  border-color: red;
}
</style>
