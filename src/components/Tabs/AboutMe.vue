<template>
  <div class="component-wrapper">
    <div class="content-wrapper my-image">
      <img :src="require('/src/assets/jav2.jpg')">
    </div>
    <div class="content-wrapper text">
      {{ loremIpsum }}
    </div>
  </div>
</template>

<script>
import Constants from "../Constants";

export default {
  name: "AboutMe",
  mixins: [Constants],
}
</script>

<style scoped lang="scss">
.component-wrapper{
  display: flex;
  flex-direction: row;
  .content-wrapper{
    flex-grow: 1;
    flex-basis: 0;
    &.text{
      padding: 100px 80px;
      font-size: 18px;
      text-align: left;
      @media screen and (max-width: 700px) {
        padding: 20px 10px;
      }
    }
    &.my-image{
      display: flex;
      justify-content: center;
      align-items: center;
    }
  }
}
</style>