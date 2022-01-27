<template>
  <div>
    <div class="container">
      <HeadingBlock class="title" :text="'Follow Us:'" />
      <div class="socials">
        <a
          v-for="(social, i) in socials"
          :key="i"
          :href="social.link"
          class="social-item"
        >
          <img :src="social.image" />
          <HeadingBlock
            class="social-title"
            :heading-level="3"
            :text="social.title"
          />
        </a>
      </div>
    </div>
    <HeadingBlock
      class="copyright"
      :text="'Cromba is a social network project that uses blockchain among other technologies'"
    />
    <HeadingBlock
      class="copyright-sub"
      :text="'2022 Comba. All rights reserved'"
    />
  </div>
</template>

<script>
import HeadingBlock from '~/../zekoder-web-components/src/components/heading-block/HeadingBlock.vue'
export default {
  name: 'FooterVue',
  components: { HeadingBlock },
  data() {
    return {
      socials: [
        {
          title: 'Facebook',
          image: require('../assets/facebook.svg'),
          link: 'https://facebook.com',
        },
        {
          title: 'Twitter',
          image: require('../assets/twitter.svg'),
          link: 'https://twitter.com',
        },
        {
          title: 'Instagram',
          image: require('../assets/instagramm.svg'),
          link: 'https://instagram.com',
        },
        {
          title: 'Telegram',
          image: require('../assets/telegramm.svg'),
          link: 'https://telegram.com',
        },
        {
          title: 'Youtube',
          image: require('../assets/youtube.svg'),
          link: 'https://youtube.com',
        },
        {
          title: 'Github',
          image: require('../assets/mark-github.svg'),
          link: 'https://github.com',
        },
      ],
    }
  },
}
</script>

<style scoped lang="scss">
.container {
  display: flex;
  flex-direction: row;
  justify-content: flex-start;
  align-items: flex-start;
  margin: 20px;
  .title {
    font-family: Raleway;
    text-align: center;
    color: white;
    font-weight: 400;
    margin: 0;
  }
  .socials {
    display: flex;
    flex-direction: column;
    justify-content: space-around;
    align-items: flex-start;
    height: 100%;
    margin-left: 10px;
    margin-top: 5px;
    .social-item {
      display: flex;
      flex-direction: row;
      justify-content: flex-start;
      align-items: center;
      height: 100%;
      img {
        width: 20px;
        height: 20px;
      }
      .social-title {
        font-family: Raleway;
        font-size: 10px;
        color: white;
        margin-left: 10px;
      }
    }
  }
}
.copyright{
  font-family: Raleway;
  font-size: 19px;
  color: white;
  margin-top: 20px;
  text-align: center;
}
.copyright-sub{
  font-family: Raleway;
  font-size: 16px;
  color: #B6B6B6;
  margin-top: 20px;
  text-align: center;
}
</style>
