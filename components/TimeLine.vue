<template>
  <div class="container" id="cromba-timeline">
    <ZekHeading class="title" :text="'Timeline'" />
    <img class="image" src="/timeline.svg" />
  </div>
</template>

<script>
import { ZekHeading } from '@zekoder/zekoder-web-components'
export default {
  components: { ZekHeading },
  methods: {
    getImage(image) {
      return new URL(image, import.meta.url).href
    },
  },
}
</script>

<style scoped lang="scss">
.container {
  padding: 0;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  margin: 3vw;
  .title {
    font-family: Raleway;
    font-size: 36px;
    color: white;
    margin-bottom: 40px;
    @media only screen and (max-width: 768px) {
      font-size: 4vw;
    }
  }
  .image {
    width: 100%;
    height: 100%;
  }
}
</style>
