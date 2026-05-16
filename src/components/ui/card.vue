<script setup lang="ts">
import { ShoppingCartIcon, StoreIcon } from "lucide-vue-next";

interface Props {
  photo: string;
  title: string;
  price: number;
  store: string;
}

defineProps<Props>();
</script>

<template>
  <div>
    <img :src="photo" :alt="title" srcset="" />
    <div>
      <div>
        <h2>{{ title }}</h2>
        <p>${{ price.toFixed(2) }}</p>
      </div>
      <div>
        <div>
          <StoreIcon />
          <p>{{ store }}</p>
        </div>
        <Button>
          <ShoppingCartIcon />
        </Button>
      </div>
    </div>
  </div>
</template>

<style lang="css" scoped></style>
