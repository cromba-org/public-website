<template>
  <div class="container" id="cromba-features">
    <ZekHeading class="title" :text="'Cromba Amazing Features'" />
    <ZekHeading
      :heading-level="3"
      class="subtitle"
      :text="'Explore sensational features to that comes with cromba'"
    />
    <div class="cards">
      <div v-for="(card, i) in cards" :key="i" class="card">
        <div class="card-image">
          <img :src="card.image" />
        </div>
        <div class="card-content">
          <ZekHeading class="card-title" :text="card.title" />
          <ZekText class="card-desc" :text="card.text" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { ZekHeading, ZekText } from "@zekoder/zekoder-web-components";

export default {
  name: "CrombaFeatures",
  components: { ZekHeading, ZekText },
  data() {
    return {
      cards: [
        {
          image: "~/assets/feature-image-1.svg",
          title: "Transparent",
          text: "A decentralized transparent social media policy that everyone knows the policy transparently.",
        },
        {
          image: "~/assets/feature-image-2.svg",
          title: "Democratic",
          text: "Anyone can own or join any available social network.",
        },
        {
          image: "~/assets/feature-image-3.svg",
          title: "Rewarding",
          text: "Supports a variety of the most popular digital currencies and always up to date.",
        },
        {
          image: "~/assets/feature-image-4.svg",
          title: "Safe",
          text: "Users can move profiles between social networks.",
        },
      ],
    };
  },
};
</script>

<style scoped lang="scss">
.container {
  padding: 0;
  margin: 0;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  background-image: url("~/assets/bg-get-started.png");
  background-repeat: no-repeat;
  background-size: cover;
  background-position: center;
  .title {
    color: white;
    margin-bottom: 40px;
    font-family: Raleway;
  }
  .subtitle {
    color: white;
    margin-bottom: 40px;
    font-family: Roboto;
    font-weight: 400;
  }
  .cards {
    display: flex;
    flex-direction: row;
    justify-content: space-around;
    align-items: center;
    width: 100%;
    max-width: 1200px;
    margin-bottom: 40px;
    .card {
      font-family: Raleway;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: flex-start;
      width: calc(25% - 40px);
      height: 415px;
      margin: 0 20px;
      padding: 20px;
      background: rgba(255, 255, 255, 0.02);
      border: 1px solid rgba(255, 255, 255, 0.2);
      box-sizing: border-box;
      backdrop-filter: blur(200px);
      border-radius: 18px;

      .card-image {
        width: 80px;
        height: 80px;
        img {
          width: 100%;
          height: 100%;
        }
      }
      .card-content {
        width: 100%;
        height: 100%;
        display: flex;
        flex-direction: column;
        align-items: flex-start;
        .card-title {
          color: white;
          margin-bottom: 20px;
        }
        .card-desc {
          color: white;
          margin-bottom: 20px;
        }
      }
    }
  }
}
</style>
