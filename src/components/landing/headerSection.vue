<script setup lang="ts">
import Button from "../ui/button.vue";
import { User, LogIn } from "lucide-vue-next";
</script>

<template>
  <header class="header">
    <img src="/src/assets/images/logo.svg" alt="Alimentae Logo" />
    <nav class="nav">
      <ul>
        <li><a href="#home">Home</a></li>
        <li><a href="#stores">Lojas</a></li>
        <li><a href="#menu">Cardápio</a></li>
        <li><a href="#about">Sobre</a></li>
        <li><a href="#contact">Contato</a></li>
      </ul>
    </nav>

    <div class="container-buttons">
      <Button variant="primary">
        <User />
        Criar Conta</Button
      >
      <Button variant="terciary">
        <LogIn />
        Login
      </Button>
    </div>
  </header>
</template>

<style lang="css" scoped>
.header {
  display: grid;
  grid-template-columns: 1fr auto 1fr;
  align-items: center;

  padding: 0.8rem 1.2rem;

  img {
    justify-self: start;
    width: 3rem;
    border-radius: 0.2rem;
  }
}
.nav {
  justify-self: center;
  ul {
    display: flex;
    list-style: none;
    gap: 2rem;
  }

  a {
    position: relative;

    text-decoration: none;
    color: var(--color-text-black);

    font-family: var(--font-primary);
    font-weight: 300;
    font-size: 1.1rem;

    transition: 0.2s ease;

    &::after {
      content: "";

      position: absolute;
      left: 0;
      bottom: -6px;

      width: 0%;
      height: 2px;

      border-radius: 999px;

      background: var(--color-accent);

      transition: width 0.3s ease;
    }

    &:hover {
      color: var(--color-accent);

      transform: translateY(-2px);
    }

    &:hover::after {
      width: 100%;
    }
  }
}
.container-buttons {
  display: flex;
  gap: 0.5rem;
}
</style>
