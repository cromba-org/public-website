<template>
  <div class="nav">
    <img class="logo" src="../assets/logo-no-words.svg" />
    <div class="buttons">
      <ActionButton class="button" :label="`Home`" />
      <ActionButton class="button" :label="`About Us`" />
      <ActionButton class="button" :label="`Features`" />
      <ActionButton class="button" :label="`Our Team`" />
      <ActionButton class="button" :label="`Timeline`" />
      <ActionButton class="button" :label="`Ecosystem`" />
      <ActionButton class="button" :label="`Contact Us`" />
    </div>
  </div>
</template>

<script>
import ActionButton from '../../zekoder-web-components/src/components/action-button/ActionButton.vue'
export default {
  name: 'NavBar',
  components: {
    ActionButton,
  },
}
</script>

<style scoped lang="scss">
.nav {
  display: flex;
  justify-content: space-around;
  align-items: center;
  padding: 0 20px;
  height: 90px;
  background-color: #11011e;
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
        color: #A6CE39;
      }
    }
  }
}
</style>
