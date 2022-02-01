<template>
  <div class="nav">
    <img class="logo" :src="getImage('../assets/logo-no-words.svg')" />
    <div class="buttons">
      <a href="#cromba-home"><ZekButton class="button" :label="`Home`" /> </a>
      <a href="#about-cromba"><ZekButton class="button" :label="`About Us`" /> </a>
      <a href="#cromba-features"><ZekButton class="button" :label="`Features`" /> </a>
      <a href="#cromba-team"><ZekButton class="button" :label="`Our Team`" /> </a>
      <a href="#cromba-timeline"><ZekButton class="button" :label="`Timeline`" /> </a>
      <a href="#cromba-ecosystem"><ZekButton class="button" :label="`Ecosystem`" /> </a>
      <a href="#join-us"><ZekButton class="button" :label="`Contact Us`" /> </a>
    </div>
  </div>
</template>

<script>
import { ZekButton } from "@zekoder/zekoder-web-components";
export default {
  name: "NavBar",
  components: {
    ZekButton,
  },
  methods: {
    getImage(image) {
      return new URL(image, import.meta.url).href;
    },
  }
};
</script>

<style scoped lang="scss">
.nav {
  display: flex;
  justify-content: space-around;
  align-items: center;
  padding: 0 20px;
  height: 90px;
  width: 100%;
  max-width: 100vw;
  .logo {
    width: 150px;
    height: 100%;
    margin-right: 20px;
  }
  .buttons {
    display: flex;
    justify-content: space-around;
    align-items: center;
    .button {
      width: 100px;
      height: 40px;
      color: #ffffff;
      font-size: 14px;
      font-weight: bold;
      border: none;
      outline: none;
      background-color: transparent;
      cursor: pointer;
      &:hover {
        color: #a6ce39;
      }
    }
  }
}
</style>
