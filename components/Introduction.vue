<template>
  <div class="container" id="cromba-home">
    <NavBar />
    <div class="introduction">
      <div class="left-section">
        <ZekHeading
          :text="'Cromba is open source for the free world'"
          class="heading-block"
        />
        <ZekText
          :text="'Cromba is not another fancy blockchain project, Cromba is a social network project that uses blockchain among other technologies'"
          :line-breaks="2"
          class="text-block"
        />
        <a class="buttons">
          <ZekButton :label="'WHITEPAPER'" :url="'https://docs.google.com/document/d/1eVtp4VGARtySsDcZ1UFwq06pCPlV2Cs7A9k1diRobjo/edit?usp=sharing'"/>
          &nbsp;
          <ZekButton :label="'CONTRACT'" />
        </a>
      </div>
      <div class="right-section">
        <img src="/logo.svg" v-if="!md.mobile()" />
      </div>
    </div>
  </div>
</template>

<script>
import { ZekHeading, ZekText, ZekButton } from '@zekoder/zekoder-web-components'
import MobileDetect from 'mobile-detect';

export default {
  name: 'IntroductionBlock',
  components: {
    ZekText,
    ZekButton,
    ZekHeading,
  },
  data(){
    return {
      md: new MobileDetect(window.navigator.userAgent),
    }
  },
  methods: {
    getImage(image) {
      return new URL(image, import.meta.url).href
    },
  },
}
</script>

<style scoped lang="scss">
.container {
  background-image: url('~/assets/bg-above-the-fold.png');
  background-repeat: no-repeat;
  background-size: cover;
  background-position: center;
  width: 100%;

  .introduction {
    display: flex;
    flex-direction: row;
    justify-content: space-around;
    align-items: center;
    width: 100%;
    height: 100%;
    @media only screen and (hover: none) and (pointer: coarse) {
      flex-direction: column;
    }
    .right-section {
      width: 50%;
      height: 100%;
      display: flex;
      justify-content: center;
      align-items: center;
      padding: 0 100px;

      img {
        width: 100%;
        height: 100%;
      }
    }
    .left-section {
      width: 50%;
      height: 100%;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      padding: 0 100px;
      text-align: left;
      @media only screen and (hover: none) and (pointer: coarse) {
        width: 75%;
        text-align: center;
      }
      .heading-block {
        font-family: Raleway;
        color: #ffffff;
        margin-bottom: 20px;
        font-weight: bold;
        font-size: 40px;
        @media only screen and (hover: none) and (pointer: coarse) {
          font-size: 4vw;
        }
      }
      .text-block {
        font-family: Roboto;
        color: #ffffff;
        font-size: 20px;
        font-weight: 400;
        @media only screen and (hover: none) and (pointer: coarse) {
          font-size: 3vw;
        }
      }
      .buttons {
        margin: 20px 0;
        display: flex;
        justify-content: space-around;
        align-items: center;
        width: 75%;
        @media only screen and (hover: none) and (pointer: coarse) {
          width: 100%;
        }
        .button {
          font-family: Roboto;
          font-weight: bold;
          font-size: 13px;
          color: #ffffff;
          width: 124px;
          height: 43px;
          background: #0a0a09;
          border: 1.5px solid #ffffff;
          box-sizing: border-box;
          border-radius: 12px;
          cursor: pointer;
        }
      }
    }
  }
}
</style>
