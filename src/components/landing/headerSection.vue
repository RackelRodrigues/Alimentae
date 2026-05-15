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

    <div>
      <Button variant="primary">
        <User />
        Criar Conta</Button
      >
      <Button variant="secondary">
        <LogIn />
        Login
      </Button>
    </div>
  </header>
</template>

<style lang="css" scoped>
.header {
  display: flex;
  justify-content: space-between;
  align-items: center;

  padding: 1rem 2rem;
}

.nav {
  ul {
    display: flex;
    list-style: none;
    gap: 2rem;
  }

  a {
    text-decoration: none;
    color: var(--color-text-black);
    font-family: var(--font-primary);
    font-weight: 300;
    font-size: 1.1;
    cursor: pointer;
  }
}
</style>
