<template>
  <div class="container" id="join-us">
    <div class="left-section">
      <ZekHeading class="title" :text="'JOIN OUR COMMUNITY'" />
      <ZekHeading
        class="subtitle"
        :heading-level="5"
        :text="'Simple and easy way to start your journey with us'"
      />
      <ZekButton
        :label="'Whitepaper'"
        :url="'https://docs.google.com/document/d/1eVtp4VGARtySsDcZ1UFwq06pCPlV2Cs7A9k1diRobjo/edit?usp=sharing'"
      />
    </div>
    <div class="right-section">
      <div v-for="(card, i) in cards" :key="i" class="card">
        <img class="card-image" :src="card.image" />
        <div class="card-content">
          <ZekHeading
            class="card-title"
            :heading-level="3"
            :text="card.title"
          />
          <ZekText
            class="card-subtitle"
            :heading-level="3"
            :text="card.subtitle"
          />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { ZekHeading, ZekText, ZekButton } from '@zekoder/zekoder-web-components'

export default {
  components: { ZekHeading, ZekButton, ZekText },
  data() {
    return {
      cards: [
        {
          image: '/get-started-icon-frame.svg',
          title: 'As a Developer',
          subtitle: 'Your account and personal identity are guaranteed safe.',
        },
        {
          image: '/get-started-icon-frame-2.svg',
          title: 'As a Partner',
          subtitle: 'Join our community and invest in us',
        },
        {
          image: '/get-started-icon-frame-3.svg',
          title: 'As an Early-Bird',
          subtitle: 'Buy and sell popular currencies and keep track of them.',
        },
      ],
    }
  },
  methods: {
    getImage(image) {
      return new URL(image, import.meta.url)
    },
  },
}
</script>

<style scoped lang="scss">
.container {
  display: flex;
  flex-direction: row;
  justify-content: space-around;
  align-items: center;
  width: 100%;
  height: 100%;
  margin: 20px 0;
  @media only screen and (hover: none) and (pointer: coarse) {
    flex-direction: column;
    align-items: flex-start;
  }
  .left-section {
    width: 50%;
    height: 100%;
    display: flex;
    flex-direction: column;
    justify-content: flex-start;
    align-items: flex-start;
    padding: 0 100px;
    @media only screen and (hover: none) and (pointer: coarse) {
      font-size: 4vw;
      padding: 0 3vw;
    }
    .title {
      font-family: Raleway;
      font-size: 36px;
      color: white;
      margin-bottom: 40px;
      @media only screen and (hover: none) and (pointer: coarse) {
        font-size: 4vw;
        margin-bottom: 0;
      }
    }
    .subtitle {
      font-family: Raleway;
      font-weight: 400;
      font-size: 18px;
      color: white;
      margin-bottom: 40px;
      @media only screen and (hover: none) and (pointer: coarse) {
        font-size: 3vw;
      }
    }
    .button {
      font-family: Raleway;
      font-weight: bold;
      font-size: 13px;
      color: #ffffff;
      width: 190px;
      height: 43px;
      background: #0a0a09;
      border: 1.5px solid #ffffff;
      box-sizing: border-box;
      border-radius: 12px;
      cursor: pointer;
    }
  }
  .right-section {
    width: 50%;
    height: 100%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    padding: 0 100px;
    @media only screen and (hover: none) and (pointer: coarse) {
      padding: 0 3vw;
      width: calc(100% - 6vw);
      margin-top: 5vh;
    }
    .card {
      padding: 10px 52px 20px 20px;
      width: 100%;
      height: 128px;
      background: rgba(255, 255, 255, 0.02);
      border: 1px solid rgba(255, 255, 255, 0.05);
      box-sizing: border-box;
      border-radius: 18px;
      display: flex;
      flex-direction: row;
      justify-content: flex-start;
      align-items: center;
      margin: 10px 0;

      .card-image {
        width: 80px;
        height: 80px;
        margin: 20px;
      }
      .card-content {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: flex-start;
        .card-title {
          font-family: Raleway;
          font-size: 20px;
          color: white;
          font-weight: 600;
          margin: 5px 0;
          @media only screen and (hover: none) and (pointer: coarse) {
            font-size: 4vw;
          }
        }
        .card-subtitle {
          font-family: Roboto;
          font-weight: 400;
          font-size: 16px;
          color: #b6b6b6;
          margin: 5px 0;
          @media only screen and (hover: none) and (pointer: coarse) {
            font-size: 3vw;
          }
        }
      }
    }
  }
}
</style>
