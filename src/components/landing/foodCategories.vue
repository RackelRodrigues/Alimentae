<script setup lang="ts">
import {
  PizzaIcon as Pizza,
  BeefIcon as Beef,
  SaladIcon as Salad,
  SandwichIcon as Sandwich,
  IceCreamIcon as IceCream,
  SoupIcon as Soup,
  CoffeeIcon as Coffee,
  FishIcon as Fish,
  DrumstickIcon as Drumstick,
  CupSodaIcon as CupSoda,
} from "lucide-vue-next";

const foodCategories = [
  {
    title: "Pizzas",
    icon: Pizza,
  },
  {
    title: "Hambúrgueres",
    icon: Beef,
  },
  {
    title: "Saudável",
    icon: Salad,
  },
  {
    title: "Lanches",
    icon: Sandwich,
  },
  {
    title: "Sobremesas",
    icon: IceCream,
  },
  {
    title: "Sopas",
    icon: Soup,
  },
  {
    title: "Cafés",
    icon: Coffee,
  },
  {
    title: "Frutos do Mar",
    icon: Fish,
  },
  {
    title: "Frango",
    icon: Drumstick,
  },
  {
    title: "Bebidas",
    icon: CupSoda,
  },
];
</script>

<template>
  <div class="containerFoodCategories">
    <div
      v-for="category in foodCategories"
      :key="category.title"
      class="category-wrapper"
    >
      <div class="category-card">
        <component
          class="category-icon"
          :is="category.icon"
          :size="32"
          color="black"
        />
      </div>

      <span class="category-name">
        {{ category.title }}
      </span>
    </div>
  </div>

  <div class="foods">outras comidas aqui</div>
</template>

<style lang="css" scoped>
.containerFoodCategories {
  display: flex;
  align-items: center;
  gap: 1.5rem;
  background-color: var(--color-primary);
  width: 100%;
  padding: 1.5rem 0.5rem;
  overflow-x: auto;
}

.category-wrapper {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 0.2rem;
  width: 100%;
}

.category-card {
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 1rem;
  padding: 2rem;

  width: 3rem;
  height: 3rem;
  /* padding: 1rem; */

  border-radius: 50rem;

  background-color: var(--color-accent);
  color: var(--color-white);

  cursor: pointer;
  transition: background-color 0.2s ease;
}

.category-icon svg {
  width: 2rem;
  height: 2rem;
  color: var(--color-white);
}

.category-card:hover {
  background-color: var(--color-accent-hover);
}

.category-name {
  font-family: var(--font-primary);
  font-size: 0.9rem;
  font-weight: 300;
  color: var(--color-white);
  text-align: center;
}

.category-icon svg {
  width: 2rem;
  height: 2rem;
  color: var(--color-white);
}

.foods {
  text-align: center;
  height: 50vh;
}
</style>
