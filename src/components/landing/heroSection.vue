<script setup lang="ts">
import * as Input from "../ui/input/index";
import {
  Sparkles,
  UserStar,
  ShieldCheckIcon,
  MapPinCheckIcon,
} from "lucide-vue-next";
</script>

<template>
  <div>
    <h1></h1>
    <p></p>
    <Input> </Input>
    <div>
      <span>
        <UserStar />
        4.8(Excelente)
      </span>
      <span>
        <Sparkles />
        1.00 Restaurantes disponiveis
      </span>

      <span>
        <ShieldCheckIcon />
        Entrega mèdia entre 30 min.
      </span>
    </div>
    <img
      src="src/assets/images/foodAlimentae.svg"
      alt="Imagem de um prato de comida"
    />
  </div>
</template>

<style lang="css" scoped></style>
