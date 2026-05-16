<script setup lang="ts">
import Button from "../ui/button.vue";
import { Input } from "../ui/input/index";
import {
  Sparkles,
  UserStar,
  ShieldCheckIcon,
  MapPinCheckIcon,
  UtensilsCrossedIcon,
} from "lucide-vue-next";
</script>

<template>
  <div class="containerHero">
    <div>
      <h1 class="title">
        Peça dos <span> Melhores Restaurantes </span> perto de voce
      </h1>
      <p class="subtitle">
        Descubra Retaurantes na sua região e peça online com entrega rápida
      </p>
      <Input.Root>
        <MapPinCheckIcon color="var(--color-accent-hover)" />
        <Input.Field placeholder="Digite seu endereço de entrega" />
        <div class="containerButton">
          <Button variant="secondary">ver Restaurantes</Button>
        </div>
      </Input.Root>
      <div class="container-info">
        <div class="info-group">
          <span class="emphasis">
            <UserStar class="star" />
            4.8(Excelente)
          </span>
          <span class="emphasis">
            <UtensilsCrossedIcon class="utensils" />
            1,000 Restaurantes disponiveis
          </span>
        </div>

        <span class="emphasis">
          <ShieldCheckIcon class="check" />
          Entrega mèdia entre 30 min.
        </span>
      </div>
    </div>

    <img
      src="/src/assets/images/hero-image.svg"
      alt="Imagem de um prato de comida"
    />
  </div>
  <div class="filtro"></div>
</template>

<style lang="css" scoped>
.containerHero {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
  background-color: var(--color-hero);
  height: 75vh;
  /* gap: 2rem; */
  img {
    width: 45rem;
  }
}

/* .containerButton {
  padding: 1rem;
} */

.container-info {
  display: flex;
  flex-direction: column;
  /* justify-content: space-between; */
  align-items: center;
  /* justify-items: center; */
  gap: 1rem;
  margin-top: 3rem;
  width: 100%;
  padding-inline: 2rem;

  span {
    cursor: pointer;
    transition: 0.2s ease;
    align-items: center;
  }

  .info-group {
    display: flex;
    gap: 2rem;
    justify-content: space-between;
  }
}

.emphasis {
  font-family: var(--font-primary);
  font-weight: 400;
  font-size: 0.9rem;
}

.star {
  color: var(--color-rating);
  /* fill: var(--color-rating); */
}

.utensils {
  color: var(--color-primary);
}
.check {
  color: var(--color-accent);
}

.filtro {
  width: 100%;
  background-color: var(--color-accent-hover);
}

.title {
  font-size: 2.5rem;
  font-weight: bold;
  font-family: var(--font-fredoka);
  margin-bottom: 1rem;
  width: 40rem;

  span {
    color: var(--color-primary-hover);
  }
}

.subtitle {
  font-family: var(--font-primary);
  font-size: 1.2rem;
  font-weight: 200;
  /* margin-top: 0.5rem;*/
  margin-bottom: 1.5rem;
}
</style>
