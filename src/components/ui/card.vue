<script setup lang="ts">
import { ShoppingCartIcon, StoreIcon, Heart } from "lucide-vue-next";
import Button from "./button.vue";
import { ref } from "vue";

const liked = ref(false);

interface Props {
  photo?: string;
  title: string;
  price: number;
  store: string;
}

defineProps<Props>();

function toggleLike() {
  console.log("Toggling like...");
  liked.value = !liked.value;
  console.log(liked.value ? "Liked!" : "Unliked!");
}
</script>

<template>
  <div class="container-card">
    <div class="image-wrapper">
      <Heart class="heart-icon" @click="toggleLike" />
      <img :src="photo" :alt="title" />
    </div>
    <div class="content-card">
      <div class="card-info">
        <h2>{{ title }}</h2>
        <p>${{ price.toFixed(2) }}</p>
      </div>
      <div class="card-store">
        <div>
          <StoreIcon class="card-icon" />
          <p>{{ store }}</p>
        </div>
        <Button variant="terciary">
          <ShoppingCartIcon class="card-icon" />
        </Button>
      </div>
    </div>
  </div>
</template>

<style lang="css" scoped>
.container-card {
  display: flex;
  flex-direction: column;
  /* gap: 0.5rem; */

  width: 100%;
  max-width: 300px;

  background: linear-gradient(
    to bottom,
    transparent 0%,
    transparent 50%,
    var(--color-accent) 50%,
    var(--color-accent) 100%
  );
  border-radius: 0 0 2rem 2rem;

  img {
    width: 100%;
    height: auto;
    border-radius: 2rem;
    object-fit: cover;
  }
}
.image-wrapper {
  position: relative;
}

.heart-icon {
  position: absolute;
  top: 1rem;
  right: 1rem;
  z-index: 10;
  cursor: pointer;
  padding: 0.5rem;
  border-radius: 0.5rem;
  background-color: rgba(255, 255, 255, 0.9);
  width: 2rem;
  height: 2rem;
  color: var(--color-accent);
}

.heart-icon:hover {
  background-color: rgba(255, 255, 255, 1);
}

.content-card {
  display: flex;
  flex-direction: column;
  padding: 1rem;
  align-items: center;
  background-color: var(--color-accent);
  border-radius: 0 0 2rem 2rem;
  gap: 1rem;
  h2 {
    font-size: 1.2rem;
    font-weight: bold;
    color: var(--color-white);
    cursor: pointer;
  }

  p {
    font-size: 1.2rem;
    font-weight: 800;
    color: var(--color-white);
    cursor: pointer;
  }

  /* div {
    display: flex;
   
  } */
}

.card-icon {
  width: 1.5rem;
  height: 1.5rem;
  color: var(--color-white);
}
.card-info {
  display: flex;
  align-items: center;
  width: 100%;
  justify-content: space-between;
}

.card-store {
  display: flex;
  align-items: center;
  width: 100%;
  justify-content: space-between;

  > div {
    display: flex;
    align-items: center;
    /* gap: 0.5rem; */
    /* gap: 0.5rem; */
  }
}
</style>
