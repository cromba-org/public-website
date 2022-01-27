<template>
  <div class="container">
    <div class="left-section">
      <HeadingBlock class="title" :text="'JOIN OUR COMMUNITY'" />
      <HeadingBlock
        class="subtitle"
        :heading-level="5"
        :text="'Simple and easy way to start your journey with us'"
      />
      <ActionButton :label="'Whitepaper'" />
    </div>
    <div class="right-section">
      <div v-for="(card,i) in cards" :key="i" class="card">
        <img class="card-image" :src="card.image" />
        <div class="card-content">
          <HeadingBlock
            class="card-title"
            :heading-level="3"
            :text="card.title"
          />
          <TextBlock
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
import HeadingBlock from '~/../zekoder-web-components/src/components/heading-block/HeadingBlock.vue'
import ActionButton from '~/../zekoder-web-components/src/components/action-button/ActionButton.vue'
import TextBlock from '~/../zekoder-web-components/src/components/text-block/TextBlock.vue'
export default {
  components: { HeadingBlock, ActionButton, TextBlock },
  data(){
    return {
      cards: [
        {
          image: require('../assets/get-started-icon-frame.svg'),
          title: 'As a Developer',
          subtitle: 'Your account and personal identity are guaranteed safe.',
        },
        {
          image: require('../assets/get-started-icon-frame-2.svg'),
          title: 'As a Partner',
          subtitle: 'Join our community and invest in us',
        },
        {
          image: require('../assets/get-started-icon-frame-3.svg'),
          title: 'As an Early-Bird',
          subtitle: 'Buy and sell popular currencies and keep track of them.',
        },
      ]
    }
  }
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
  .left-section {
    width: 50%;
    height: 100%;
    display: flex;
    flex-direction: column;
    justify-content: flex-start;
    align-items: flex-start;
    padding: 0 100px;
    .title {
      font-family: Raleway;
      font-size: 36px;
      color: white;
      margin-bottom: 40px;
    }
    .subtitle {
      font-family: Raleway;
      font-weight: 400;
      font-size: 18px;
      color: white;
      margin-bottom: 40px;
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
        }
        .card-subtitle {
          font-family: Roboto;
          font-weight: 400;
          font-size: 16px;
          color: #B6B6B6;
          margin: 5px 0;
        }
      }
    }
  }
}
</style>
