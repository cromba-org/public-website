<template>
  <div class="container">
    <ZekHeading class="title" :text="'Distribution Plan'" />
    <img class="image" src="/distribution-plan.svg" />
  </div>
</template>

<script>
import { ZekHeading } from "@zekoder/zekoder-web-components";
export default {
  components: { ZekHeading },
  methods: {
    getImage(image) {
      return new URL(image, import.meta.url).href;
    },
  }
};
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
