<template>
  <div class="nav">
    <img class="logo" src="~/assets/logo-no-words.svg" />
    <div class="buttons">
      <ZekButton class="button" :label="`Home`" />
      <ZekButton class="button" :label="`About Us`" />
      <ZekButton class="button" :label="`Features`" />
      <ZekButton class="button" :label="`Our Team`" />
      <ZekButton class="button" :label="`Timeline`" />
      <ZekButton class="button" :label="`Ecosystem`" />
      <ZekButton class="button" :label="`Contact Us`" />
    </div>
  </div>
</template>

<script>
import { ZekButton } from "@zekoder/zekoder-web-components";
export default {
  name: "NavBar",
  components: {
    ZekButton,
  },
};
</script>

<style scoped lang="scss">
.nav {
  display: flex;
  justify-content: space-around;
  align-items: center;
  padding: 0 20px;
  height: 90px;
  width: 100%;
  max-width: 100vw;
  .logo {
    width: 150px;
    height: 100%;
    margin-right: 20px;
  }
  .buttons {
    display: flex;
    justify-content: space-around;
    align-items: center;
    .button {
      width: 100px;
      height: 40px;
      color: #ffffff;
      font-size: 14px;
      font-weight: bold;
      border: none;
      outline: none;
      background-color: transparent;
      cursor: pointer;
      &:hover {
        color: #a6ce39;
      }
    }
  }
}
</style>
