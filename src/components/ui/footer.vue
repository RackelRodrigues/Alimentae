<script>
import Button from "./button.vue";
import { IoLogoInstagram } from "react-icons/io5";
import { FaFacebook, FaLinkedinIn } from "react-icons/fa6";
import { FaLinkedin } from "react-icons/fa";
</script>

<template>
  <footer>
    <div class="firstline">
      <div>
        <img src="../../assets/images/logo.svg" />
        <span>linha</span>
        <p>
          O Alimentae conecta você aos melhores estabelecimentos da sua região
          com rapidez e qualidade.
        </p>
      </div>

      <div>
        <h2>Companhia</h2>
        <a href="">Sobre nós</a>
        <a href="">Carreiras</a>
        <a href="">Blog</a>
      </div>

      <div>
        <h2>Para usuários</h2>
        <a href="">Como funciona</a>
        <a href="">Suporte</a>
        <a href="">FAQ</a>
      </div>
      <div>
        <h2>Para parceiros</h2>
        <a href="">seja parceiro</a>
        <a href="">Area do restaurante</a>
      </div>
    </div>
    <div class="secondline">
      <Button> App Store </Button>
      <button>Google Play</button>

      <div>
        <div>
          <h2>Legal</h2>
        </div>
        <a href="">Termos de uso</a>
        <a href="">Política de privacidade</a>
      </div>

      <span class="social-action">
        <FaLinkedinIn class="social-icon" />
      </span>
      <span class="social-action">
        <IoLogoInstagram class="social-icon" />
      </span>
      <span class="social-action">
        <FaFacebook class="social-icon" />
      </span>
    </div>
    <span class="footer-line">line</span>
    <p>cnpj: 00.000.000/0000-00</p>
  </footer>
</template>

<style lang="css" scoped>
.footer-line {
  display: block;
  width: 100%;
  height: 2px;
  background-color: white;
}
</style>
