<template>
  <div class="container">
    <div class="left-section">
      <div class="point">
        <ZekHeading class="title" :text="aboutCromba.label" />
        <ZekList class="list" :list-items="aboutCromba.list" />
      </div>
      <div class="point">
        <ZekHeading class="title" :text="crombaActors.label" />
        <ZekList class="list" :list-items="crombaActors.list" />
      </div>
      <div class="point">
        <ZekHeading class="title" :text="crombaSecurity.label" />
        <ZekList class="list" :list-items="crombaSecurity.list" />
      </div>
    </div>
    <div class="right-section">
      <img src="../assets/Features.svg" />
    </div>
  </div>
</template>

<script>
import { ZekHeading, ZekList } from "@zekoder/zekoder-web-components";

export default {
  components: { ZekHeading, ZekList },
  data() {
    return {
      aboutCromba: {
        label: "About Cromba",
        list: [
          "Cromba is a modern transparent, secure, democratic and rewarding social network owned by users and managed decentrally.",
          "To establish the ecosystem, ensure privacy, security and transparency. Cromba is backed by a blockchain.",
          "P2P and other technologies collectively named Cromba network and relies on CRMB cryptocurrency for value transfer.",
        ],
      },
      crombaActors: {
        label: "Cromba Actors",
        list: [
          "Validator (miner)",
          "DAO",
          "General purpose",
          "Network Operator",
          "Infra provider",
          "Contributor (the ordinary social network user)",
        ],
      },
      crombaSecurity: {
        label: "Cromba Security",
        list: [
          "No email/phone required for registration",
          "Easy Blockchain based unbreakable login",
          "No IP or Location tracing",
          "Covert when used from mobile apps",
          "Secure transactions using blockchain",
          "Secure untraceable cryptocurrency",
        ],
      },
    };
  },
};
</script>

<style scoped lang="scss">
.container {
  display: flex;
  flex-direction: row;
  justify-content: space-around;
  align-items: center;
  width: 100%;
  .left-section {
    width: 50%;
    height: 100%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: flex-start;
    padding: 0 150px;
    .title {
      color: white;
      font-family: Raleway;
      font-size: 27px;
    }

    .list {
      color: white;
      font-family: Raleway;
      font-weight: 400;
      font-size: 27px;
    }
  }
  .right-section {
    width: 50%;
    height: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 0 150px;
  }
}
</style>
