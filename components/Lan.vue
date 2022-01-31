<template>
  <div class="background">
    <div class="container">
      <div class="text-container">
        <ZekHeading class="title" :text="'LAN'" />
        <ZekText
          :text="'A big social media provider disclosed Lan’s IP address and other information to a government non tolerable for free speech, she needs a safer social not dependent on companies with government relations.'"
          class="text"
        />
      </div>
    </div>
  </div>
</template>

<script>
import { ZekHeading, ZekText } from "@zekoder/zekoder-web-components";

export default {
  name: "LanDetail",
  components: { ZekHeading, ZekText },
};
</script>

<style scoped lang="scss">
.background {
  background-image: url("../assets/bg-features.png");
  background-repeat: no-repeat;
  background-size: cover;
  background-position: center;
  width: 100%;
}
.container {
  width: 100%;
  text-align: center;
  background-image: url("../assets/Lan.svg");
  background-repeat: no-repeat;
  background-size: contain;
  background-position: center;
  background-position-x: 48%;
  height: 1058px;
  .text-container {
    width: 100%;
    height: 100%;
    padding-top: 125px;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    .title {
      font-family: "Josefin Sans";
      width: 66px;
      height: 48px;
      color: black;
    }
    .text {
      font-family: "Raleway";
      color: black;
      width: 590px;
      line-height: 1.5;
    }
  }
}
</style>
