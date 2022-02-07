<script setup>
  const menu = useState('menu', () => false);
</script>
<template>
  <div class="nav">
    <img class="logo" src="/logo-no-words.svg" />
    <img v-if="md.mobile()" src="~/assets/menu.svg" class="menu-button" @click="menu = !menu" />
    <div class="buttons" v-else >
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
import MobileDetect from 'mobile-detect';
export default {
  name: "NavBar",
  components: {
    ZekButton,
  },
  data(){
    return {
      md: new MobileDetect(window.navigator.userAgent),
    }
  },
  methods: {
    getImage(image) {
      return new URL(image, import.meta.url).href;
    },
  },
  mounted() {
    console.log(this.md.mobile())
  },
};
</script>

<style scoped lang="scss">
.nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
  height: 90px;
  width: 100%;
  max-width: 100vw;
  .logo {
    width: 150px;
    height: 100%;
    margin-left: 20px;
  }
  .menu-button {
    width: 30px;
    height: 100%;
    padding: 0 20px;
    cursor: pointer;
  }
  .buttons {
    display: flex;
    justify-content: space-around;
    align-items: center;
    margin-right: 10%;
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
