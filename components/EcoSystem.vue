<template>
  <div class="container" id="cromba-ecosystem">
    <ZekHeading class="title" :text="'Ecosystem'" />
    <div class="rows">
      <div v-for="(row, i) in rows" :key="i" class="row">
        <ZekHeading class="row-title" :text="row.label" />
        <div v-for="(item, j) in row.items" :key="j" class="row-item">
          <ZekHeading
            class="item-text"
            :text="item"
            :style="{ color: row.color }"
          />
        </div>
      </div>
    </div>
    <div class="image-container">
      <img class="image" src="/social-networks.svg" />
    </div>
  </div>
</template>

<script>
import { ZekHeading } from '@zekoder/zekoder-web-components'
export default {
  components: { ZekHeading },
  data() {
    return {
      rows: [
        {
          label: 'EARN',
          color: '#a6ce39',
          items: [
            'Appreciated Owned Content',
            'Social Network Enriching Activities',
            'Verification (mining)',
            'Digital Product Sales',
            'Infrastructure Provision',
            'Crypto Exchange',
          ],
        },
        {
          label: 'SPEND',
          color: '#00AEEF',
          items: [
            'Content Application',
            'Infrastructure Utilization',
            'Advertisment',
            'Digital Product Purchase',
          ],
        },
        {
          label: 'STAKING',
          color: '#FFCB05',
          items: [
            'Network Ownership',
            'DAO Ownership',
            'Verfication Contribution',
          ],
        },
      ],
    }
  },
  methods: {
    getImage(image) {
      return new URL(image, import.meta.url).href
    },
  },
}
</script>

<style scoped lang="scss">
.container {
  width: 100%;
  text-align: center;
  margin: 50px 0;
  .title {
    font-family: Raleway;
    font-size: 36px;
    color: white;
    @media only screen and (hover: none) and (pointer: coarse) {
      font-size: 4vw;
    }
  }
  .rows {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    width: 100%;
    @media only screen and (hover: none) and (pointer: coarse) {
      flex-direction: row;
      align-items: flex-start;
    }
    .row {
      display: flex;
      flex-direction: row;
      justify-content: flex-start;
      align-items: center;
      justify-content: flex-start;
      width: 100%;
      padding: 0 50px;
      margin: 20px 0;
      @media only screen and (hover: none) and (pointer: coarse) {
        flex-direction: column;
        width: 25%;
        padding: 0 3%;
      }
      .row-title {
        font-family: Raleway;
        font-size: 24px;
        color: white;
        transform: rotate(-90deg);
        width: 100px;
        @media only screen and (hover: none) and (pointer: coarse) {
          transform: rotate(0deg);
          font-size: 3vw;
          width: 100%;
        }
      }
      .row-item {
        width: calc((100% - 220px) / 7);
        height: 200px;
        background: rgba(255, 255, 255, 0.1);
        box-shadow: inset 0px -5px 0px rgb(250 250 250 / 15%);
        border-radius: 20px;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        margin: 0 10px;
        @media only screen and (hover: none) and (pointer: coarse) {
          width: 100%;
          height: 15vh;
          margin: 10px 0;
        }
        .item-text {
          font-family: Raleway;
          font-size: 18px;
          color: #a6ce39;
          padding: 20px;
          @media only screen and (hover: none) and (pointer: coarse) {
            font-size: 3vw;
            text-align: left;
          }
        }
      }
    }
  }
  .image-container {
    margin: 5vw;
    .image {
      margin-top: 5vh;
      width: 100%;
      height: 100%;
    }
  }
}
</style>
