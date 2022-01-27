<template>
  <div class="container">
    <div v-for="(card, i) in cards" :key="i" class="card">
      <img
        class="card-image"
        :src="card.image"
        :style="{ backgroundImage: `url('${card.background}')` }"
      />
      <HeadingBlock class="card-title" :heading-level="3" :text="card.title" />
      <TextBlock
        class="card-subtitle"
        :heading-level="3"
        :text="card.subtitle"
      />
    </div>
  </div>
</template>

<script>
import HeadingBlock from '~/../zekoder-web-components/src/components/heading-block/HeadingBlock.vue'
import TextBlock from '~/../zekoder-web-components/src/components/text-block/TextBlock.vue'
export default {
  components: { HeadingBlock, TextBlock },
  data() {
    return {
      cards: [
        {
          image: require('../assets/ahmed-sheleby.svg'),
          title: 'Ahmed Shalaby',
          subtitle:
            '20 years experience in technolgy nitch and also a co-founder of various firms in Canada, Us, Turkey and Egypt.',
          background: require('../assets/image-frame.svg'),
        },
        {
          image: require('../assets/mohamed-hany.svg'),
          title: 'Mohamed Hany',
          subtitle:
            '6 years experience as a DevOps and full stack software engineer',
          background: require('../assets/image-frame-2.svg'),
        },
        {
          image: require('../assets/mohamed-ali.svg'),
          title: 'Mohamed Ali',
          subtitle: '5 years experience in marketing and business development',
          background: require('../assets/image-frame-3.svg'),
        },
      ],
    }
  },
}
</script>

<style lang="scss" scoped>
.container {
  display: flex;
  flex-direction: row;
  .card {
    text-align: center;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    margin: 20px;
    width: calc(33% - 40px);
    height: 486px;
    background: rgba(255, 255, 255, 0.05);
    box-shadow: 0px 1px 10px rgba(0, 0, 0, 0.1);
    border-radius: 50px;
    .card-image {
      background-repeat: no-repeat;
      background-size: 73%;
      background-position: center;
      background-position-y: 45%;
      width: 270px;
      height: 270px;
    }
    .card-title {
      font-family: Raleway;
      font-size: 36px;
      color: white;
      margin-bottom: 10px;
    }
    .card-subtitle {
      font-family: Raleway;
      font-size: 18px;
      color: white;
      margin: 20px;
    }
  }
}
</style>
