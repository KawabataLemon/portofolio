<template lang="pug">
  .container
    navigation-header(:current-page="'about'")
    section.contents
      .leftContents
        section.sp-IconName
          .iconContainer
            .iconWrapper
              img(src="../static/lemon.png").iconImg
          .nameContainer
            span @KawabataLemon
        section.positionLabel
          span.contentTitle Software Engineer, Team Manager
          span.workAtLabel   Work at Coiney,Inc(hey, inc)
        section.careerLabel
          span.contentTitle Careers
          ul.careerHistoryList
            li.careerElement
              span.careerDuration 2020/03 -
              span.companyName Coiney, inc
            li.careerElement
              span.careerDuration 2019/01 - 2020/03
              span.companyName xenodata-lab.inc
            li.careerElement
              span.careerDuration 2016/10 - 2018/12
              span.companyName eureka, Inc
            li.careerElement
              span.careerDuration 2014/08 - 2016/09
              span.companyName translimit, Inc
            li.careerElement
              span.careerDuration 2014/04 - 2014/10
              span.companyName basic,Inc
            li.careerElement
              span.careerDuration 2012/05 - 2014/03
              span.companyName Adinnovation, Inc
      .rightContents
        .iconContainer
          .iconWrapper
            img(src="../static/lemon.png").iconImg
        .nameContainer
          span @KawabataLemon
    navigation-footer(:current-page="'about'")
</template>

<script lang="ts">
import Vue from 'vue'
import NavigationHeader from '../components/NavigationHeader.vue';
import NavigationFooter from '../components/NavigationFooter.vue';
export default Vue.extend({
  name: "index",
  components: {
    NavigationHeader,
    NavigationFooter
  }
})
</script>
<style lang="scss" scoped>
@import "../assets/main";
@import "../assets/mixin";



.container {
  margin: 0 auto;
  min-height: 100vh;
  background: linear-gradient(to left, $color-primary, $color-secondary);

  display: flex;
  flex-direction: column;
  justify-content: space-between;
  align-content: center;
  .header {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-content: center;
    .title {
      padding: 40px;
      span {
        @include lato;
        color: $color-accent-secondary;
        font-size: 60px;
        font-weight: bold;
      }
    }
    .navigation {
      @include mq-down() { // 引数を省略（初期値はmdの768px）
       display: none;
      }
      padding: 40px;
      a {
        text-decoration: none;
      }
      .menuItem {
        @include lato;
        color: white;
        margin: 20px;
        font-size: 40px;
        font-weight: bold;
        &.selected,
        &:hover {
          color: $color-text-accent;
          transition: 200ms;
        }
      }
    }
  }

  .contents {
    display: flex;
    flex-direction: row;
    justify-content: space-evenly;
    align-content: center;
    margin-right:12px;
    margin-left: 12px;
    .contentTitle {
      color: white;
      font-size: 48px;
      @include mq-down() {
        font-size: 22px;
      }
      font-weight: bold;
      margin-bottom: 8px;
      @include lato;
    }
    .leftContents {
      @include mq-down() {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
      }
      section {
        margin-bottom: 40px;
      }

      .sp-IconName {
        display: none;
        @include mq-down() {
          display: flex;
          flex-direction: column;
          justify-content: center;
          align-content: center;
        }
        .iconContainer {
          display: flex;
          justify-content: center;
          align-content: center;
          .iconWrapper {
            width: 200px;
            height: 200px;
            background-color: $color-accent;
            margin-bottom: 24px;
            clip-path: circle(100px at center);
            display: flex;
            justify-content: center;
            align-items: center;
            .iconImg {
              width: 180px;
              height: 180px;
              animation-name: fluffying;
              animation-iteration-count: infinite;
              animation-delay: 2000ms;
              animation-duration: 1000ms;
            }
          }
        }
        .nameContainer {
          display: flex;
          justify-content: center;
          align-content: center;
          span {
            color: white;
            font-size: 20px;
            @include lato;
          }
        }
      }
      .positionLabel {
        display: flex;
        flex-direction: column;
        .workAtLabel {
          color: $color-accent-secondary;
          margin-left: 30px;
          font-size: 35px;
          @include mq-down() {
            font-size: 24px;
          }
        }
      }

      .careerLabel {
        margin-bottom: 12px;
        ul.careerHistoryList {
          list-style: none;
          li.careerElement {
            text-decoration: none;
            margin-bottom: 8px;
            color: $color-accent-secondary;
            font-weight: bold;
            font-size: 20px;
            @include mq-down() {
              font-size: 14px;
            }

            .careerDuration {
              display: inline-block;
              width: 200px;

              @include mq-down() {
                width: 160px;
              }
            }
          }
        }
      }
    }
    .rightContents {
      @include mq-down() {
        display:none;
      }
      .iconContainer {
        .iconWrapper {
          width: 400px;
          height: 400px;
          background-color: $color-accent;
          margin-bottom: 24px;
          clip-path: circle(200px at center);
          display: flex;
          justify-content: center;
          align-items: center;
          .iconImg {
            width: 350px;
            height: 350px;
            animation-name: fluffying;
            animation-iteration-count: infinite;
            animation-delay: 2000ms;
            animation-duration: 1000ms;
          }
        }
      }
      .nameContainer {
        display: flex;
        justify-content: center;
        align-content: center;
        span {
          color: white;
          font-size: 24px;
          @include lato;
        }
      }
    }
  }
}

@keyframes rotate {
  0% { transform: rotate(0deg); }
  100% { transform: rotate(360deg); }
}

@keyframes fluffying {
  0% {
    transform: scale(1.0, 1.0);
  }
  33% {
    transform: scale(0.99, 0.99);
    transform: rotate(10deg);
  }
  66% {
    transform: scale(1.01, 1.01);
    transform: rotate(-10deg);
  }
  100% {
    transform: scale(1.0, 1.0);
  }
}

@keyframes slideIn {
from {
    margin-left: 100%;
    margin-top: 100%;
  }

  to {
    margin-left: 0%;
    margin-top: 0%;
  }
}

</style>
