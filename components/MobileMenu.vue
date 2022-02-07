<script setup>
const menu = useState('menu', () => true);
</script>

<template>
  <div class="side-menu">
    <div class="exit-container">
      <ZekButton class="exit-button" :label="'X'" @click="menu = false" />
    </div>
    <div class="buttons">
      <a href="#cromba-home"> <ZekButton class="button" :label="`Home`" /> </a>
      <a href="#about-cromba">
        <ZekButton class="button" :label="`About Us`" />
      </a>
      <a href="#cromba-features">
        <ZekButton class="button" :label="`Features`" />
      </a>
      <a href="#cromba-team">
        <ZekButton class="button" :label="`Our Team`" />
      </a>
      <a href="#cromba-timeline">
        <ZekButton class="button" :label="`Timeline`" />
      </a>
      <a href="#cromba-ecosystem">
        <ZekButton class="button" :label="`Ecosystem`" />
      </a>
      <a href="#join-us">
        <ZekButton class="button" :label="`Contact Us`" />
      </a>
    </div>
    <div class="foot-note">
      <ZekText class="text-block" :text="`2020 Cromba. All rights reserved.`" />
    </div>
  </div>
</template>

<script>
import { ZekButton, ZekText } from '@zekoder/zekoder-web-components'
export default {
  name: 'MobileMenu',
  components: {
    ZekButton,
    ZekText,
  },
}
</script>

<style lang="scss" scoped>
.side-menu {
  position: fixed;
  height: 100%;
  width: 100%;
  background-color: #11011e;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  &::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-image: url('~/assets/logo.svg');
    background-repeat: no-repeat;
    background-size: 95%;
    background-position: center;
    opacity: 0.3;
    z-index: -1;
  }
  .exit-container {
    width: 100%;
    text-align: right;
    .exit-button {
      color: #ffffff;
      font-size: 40px;
      line-height: 60px;
      border: none;
      outline: none;
      background-color: transparent;
      text-align: right;
      padding: 20px;
      cursor: pointer;
    }
  }
  .buttons {
    padding: 0 30px;
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    .button {
      width: 100%;
      color: #ffffff;
      font-size: 1.5rem;
      line-height: 3.75rem;
      border: none;
      outline: none;
      background-color: transparent;
      cursor: pointer;
    }
  }
  .foot-note {
    padding: 0 40px;
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    justify-content: flex-end;
    .text-block {
      font-family: 'Raleway';
      width: 100%;
      text-align: center;
      color: #b6b6b6;
      font-size: 0.75rem;
      line-height: 3rem;
      border: none;
      outline: none;
      background-color: transparent;
      cursor: pointer;
    }
  }
}
</style>
