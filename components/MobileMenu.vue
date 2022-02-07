<script setup>
const menu = useState('menu', () => true);
</script>

<template>
  <div class="side-menu">
    <div class="exit-container">
      <ZekButton class="exit-button" :label="'X'" @click="menu = false" />
    </div>
    <div class="buttons">
      <a v-for="(link,i) in links" :key="i" :href="link.url" @click="menu = false">
        <ZekButton class="button" :label="link.name" />
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
  data() {
    return {
      links: [
        {
          name: 'Home',
          url: '#cromba-home',
        },
        {
          name: 'About Us',
          url: '#about-cromba',
        },
        {
          name: 'Features',
          url: '#cromba-features',
        },
        {
          name: 'Our Team',
          url: '#cromba-team',
        },
        {
          name: 'Timeline',
          url: '#cromba-timeline',
        },
        {
          name: 'Ecosystem',
          url: '#cromba-ecosystem',
        },
        {
          name: 'Contact Us',
          url: '#join-us',
        },
      ]
    }
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
