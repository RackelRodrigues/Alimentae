<script setup lang="ts">
import {
  BadgeCheckIcon,
  ChartNoAxesCombined,
  BadgeCheck,
  CircleCheckBig,
} from "lucide-vue-next";
import Button from "../ui/button.vue";
</script>

<template>
  <div class="container-partner">
    <div class="content-partner">
      <div>
        <ChartNoAxesCombined class="chart" />
        <h1 class="title">
          Aumente o Faturamento do seu restaurante com o
          <span> Alimentae </span>
        </h1>
      </div>

      <p class="description">
        <span>Seu restaurante merece ser visto, lembrado e escolhido.</span>
        <span
          >O Alimentae conecta você a novos clientes, impulsiona seu faturamento
          e usa tecnologia para você focar no que faz melhor: cozinhar.</span
        >
      </p>
      <div>
        <Button variant="terciary" class="Button"
          >Quero vender na Alimentae</Button
        >
      </div>
    </div>
    <div class="image-partner">
      <img src="../../assets/images/girl.svg" alt="" />
    </div>
    <div class="container-benefits">
      <div class="benefits">
        <BadgeCheckIcon class="chart-full" />
        <h3>Mais visibilidade, Mais pedidos, Mais faturamento</h3>
      </div>
      <div class="benefits">
        <BadgeCheckIcon class="chart-normal" />
        <h3>Pagamentos seguros</h3>
      </div>
      <div class="benefits">
        <BadgeCheckIcon class="chart-full" />
        <h3>Plataforma simples e rápido</h3>
      </div>
      <div class="benefits">
        <BadgeCheckIcon class="chart-normal" />
        <h3>Suporte dedicado</h3>
      </div>
      <div class="benefits">
        <BadgeCheckIcon class="chart-full" />
        <h3>Mais clientes na sua região</h3>
      </div>
    </div>
  </div>
</template>

<style lang="css" scoped>
.container-partner {
  display: grid;
  grid-template-columns: 1fr auto 1fr;

  align-items: center;

  padding: 2rem 1.2rem;
  background-color: var(--color-primary);
  height: 70vh;
}

.container-partner img {
  width: 100%;
  max-width: 400px;

  object-fit: contain;
  display: block;
}

.content-partner {
  display: flex;
  flex-direction: column;
  gap: 2rem;
}
.Button {
  /* display: block; */
  padding: 0.8rem 0.8rem;
}

.chart {
  width: 2rem;
  height: 2rem;
  color: var(--color-white);
}

.title {
  /* display: block; */
  font-size: 2.5rem;
  font-weight: bold;
  color: var(--color-white);
  /* display: flex;
  align-items: center; */
  gap: 0.5rem;

  span {
    color: var(--color-accent);
  }
}

.description {
  font-family: var(--font-primary);
  font-size: 1.25rem;
  font-weight: 200;
  color: var(--color-white);
}

.description span {
  display: block;
  margin-top: 0.5rem;
}

.chart-full {
  width: 2rem;
  height: 2rem;
  color: var(--color-primary);
  fill: var(--color-white);
}
.chart-normal {
  width: 2rem;
  height: 2rem;
  stroke: white;
  fill: transparent;
}

.benefits {
  display: flex;
  align-items: center;
  gap: 0.5rem;
  margin-bottom: 1rem;
  span {
    font-family: var(--font-primary);
    font-size: 1.1rem;
    color: var(--color-white);
  }

  h3 {
    font-family: var(--font-primary);
    font-size: 1.2rem;
    font-weight: 300;
    color: var(--color-white);
  }
}
</style>
