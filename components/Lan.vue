<template>
  <div class="background">
    <div class="container">
      <div class="cards-container">
        <div v-for="(card, i) in cards" :key="i" class="card">
          <div class="image">
            <img :src="card.img" />
          </div>
          <ZekHeading class="title" :text="card.title" />
          <ZekText :text="card.subtitle" class="text" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { ZekHeading, ZekText } from '@zekoder/zekoder-web-components'

export default {
  name: 'LanDetail',
  components: { ZekHeading, ZekText },
  data() {
    return {
      cards: [
        {
          img: '/flaunter.svg',
          title: 'LAN',
          subtitle:
            'A big social media provider disclosed Lan’s IP address and other information to a government non tolerable for free speech, she needs a safer social not dependent on companies with government relations.',
        },
        {
          img: '/flaunter.svg',
          title: 'HATICE',
          subtitle:
            'Hatice is not comfortable with current policies and terms of the social media her children uses, She wants policies and terms matching her culture and beliefs.',
        },
        {
          img: '/flaunter.svg',
          title: 'FAISAL',
          subtitle:
            'Faisal feels not treated fairly by the giant social media platform he uses to publish his content, he believes he should be rewarded more for his efforts.',
        },
        {
          img: '/flaunter.svg',
          title: 'ALBERT',
          subtitle:
            'Albert lost access to his account where his past 10 years connections and relations left behind, he needs a guarantee no one can wipe him out from social network.',
        },
      ],
    }
  },
}
</script>

<style scoped lang="scss">
.background {
  background-image: url('~/assets/bg-features.png');
  background-repeat: no-repeat;
  background-size: cover;
  background-position: center;
  width: 100%;
}
.container {
  width: 100%;
  text-align: center;
  // background-image: url("~/assets/lan.png");
  // background-repeat: no-repeat;
  // background-size: contain;
  // background-position: center;
  // background-position-x: 48%;
  height: 100vh;
  @media only screen and (hover: none) and (pointer: coarse) {
    height: 40vh;
  }
  .cards-container {
    width: 100%;
    height: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    @media only screen and (hover: none) and (pointer: coarse) {
      height: 40vh;
    }
    .card {
      width: 20%;
      height: 80%;
      background-color: white;
      margin: 0 1%;
      box-shadow: 0px 1px 10px rgba(0, 0, 0, 0.1);
      border-radius: 5vw;
      @media only screen and (hover: none) and (pointer: coarse) {
        height: 60%;
      }
      .image {
        height: 50%;
        width: 100%;
        display: flex;
        align-items: center;
        justify-content: center;
        img {
          width: 75%;
          aspect-ratio: 1;
          border-radius: 50%;
        }
      }
      .title {
        text-align: center;
        font-family: 'Josefin Sans';
        font-size: 2vw;
        color: black;
      }
      .text {
        text-align: justify;
        font-family: 'Raleway';
        font-weight: 500;
        font-size: 1.1vw;
        color: black;
        line-height: 1.5;
        padding: 0 10%;
        @media only screen and (hover: none) and (pointer: coarse) {
          font-size: 1.3vw;
        }
      }
    }
  }
}
</style>
