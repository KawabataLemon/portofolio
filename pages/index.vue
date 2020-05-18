<template lang="pug">
  .container
    navigation-header(:current-page="'about'")
    section.contents
      .leftContents
        section.sp-IconName
          .iconContainer
            .iconWrapper
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
            border-radius: 50%;
            margin-bottom: 24px;
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
          border-radius: 50%;
          margin-bottom: 24px;
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
</style>
