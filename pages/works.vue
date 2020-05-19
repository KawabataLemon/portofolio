<template lang="pug">
.container
  navigation-header(:current-page="'works'")
  section.contents
    flip-card
      template(v-slot:front)
        .cardBase
          .imgWrapper
            img(src="../static/cn.png").logo
      template(v-slot:back)
        .cardBase
          .imgWrapper
            img(src="../static/cn.png").backlogo
    flip-card
      template(v-slot:front)
        .cardBase
          .imgWrapper
            img(src="../static/pairs.png").logo
      template(v-slot:back)
        .cardBase
          .imgWrapper
            img(src="../static/pairs.png").backlogo
    flip-card
      template(v-slot:front)
        .cardBase
          .imgWrapper
            img(src="../static/xb.png").logo
      template(v-slot:back)
        .cardBase
          .imgWrapper
            img(src="../static/xb.png").backlogo
    flip-card
      template(v-slot:front)
        .cardBase
          .imgWrapper
            img(src="../static/bd.png").logo
      template(v-slot:back)
        .cardBase
          .imgWrapper
            img(src="../static/bd.png").backlogo
    flip-card
      template(v-slot:front)
        .cardBase
          .imgWrapper
            img(src="../static/bw.png").logo
      template(v-slot:back)
        .cardBase
          .imgWrapper
            img(src="../static/bw.png").backlogo
    flip-card
      template(v-slot:front)
        .cardBase
          .imgWrapper
            img(src="../static/adstore.png").logo
      template(v-slot:back)
        .cardBase
          .imgWrapper
            img(src="../static/adstore.png").backlogo

  navigation-footer(:current-page="'works'")
</template>

<script lang="ts">
import Vue from 'vue'
import NavigationHeader from '../components/NavigationHeader.vue';
import NavigationFooter from '../components/NavigationFooter.vue';
import FlipCard from '../components/FlipCard.vue';

export default Vue.extend({
  name: "works",
  components: {
    NavigationHeader,
    NavigationFooter,
    FlipCard
  },
})
</script>

<style lang="scss" scoped>
@import "../assets/main";
@import "../assets/mixin";

@mixin lato {
  font-family: "Lato", sans-serif;
}
.container {
  margin: 0 auto;
  min-height: 100vh;
  background: linear-gradient(to left, $color-primary, $color-secondary);
  .contents{
    @include mq-down() {
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
    }
    .cardBase {
      height: 100%;
      width: 100%;
      padding: 16px;
      display:flex;
      justify-content: center;
      align-items: center;
      background-color: white;
      border-radius: 20px;
      .imgWrapper {
        display:flex;
        justify-content: center;
        align-items: center;
        .logo {
          max-width: 80%;
          max-height: 200px;
          width:auto;
          height:auto;
        }
        .backlogo {
          filter: grayscale(100%);
          opacity: 0.1;
          transform: scale(-1, 1);
          max-width: 80%;
          max-height: 200px;
          width:auto;
          height:auto;
        }
      }
    }
  }
}

</style>
