<template>
  <div class="container">
    <HeadingBlock class="title" :text="'Timeline'" />
    <img class="image" src="../assets/timeline.svg" />
  </div>
</template>

<script>
import HeadingBlock from "~/../zekoder-web-components/src/components/heading-block/HeadingBlock.vue";
export default {
    components: { HeadingBlock }
}
</script>

<style scoped lang="scss">
.container {
  padding: 0;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  margin: 50px;
  .title {
    font-family: Raleway;
    font-size: 36px;
    color: white;
    margin-bottom: 40px;
  }
  .image {
    width: 100%;
    height: 100%;
  }
}
</style>
