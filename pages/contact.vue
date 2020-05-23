<template lang="pug">
  .container
    navigation-header(:current-page="'contact'")
    section.contents
      //- .leftContents
      //-   .contentsTitle
      //-     span mail
      //-     .mailForm
      //-       .fromAccount
      //-       .mailAddress
      //-       .mailContents
      //-       .submitButton
      .rightContents
        .contentsTitle
          span Socials
        .contentsContainer
          a(href="https://www.facebook.com/LemonKawabata").socialAccount
            .socialIcon
            .socialTitle Facebook
          a(href="https://twitter.com/Kawabata_Lemon").socialAccount
            .socialIcon
            .socialTitle Twitter
          a(href="https://www.instagram.com/kawabatalemon/").socialAccount
            .socialIcon
            .socialTitle Instagram

    navigation-footer(:current-page="'contact'")
</template>

<script lang="ts">
import Vue from 'vue'
import NavigationHeader from '../components/NavigationHeader.vue';
import NavigationFooter from '../components/NavigationFooter.vue';
export default Vue.extend({
  name: "contact",
  components: {
    NavigationHeader,
    NavigationFooter
  }
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
    display: flex;
    flex-direction: row;
    justify-content: space-evenly;
    align-content: center;
    margin-right:12px;
    margin-left: 12px;
      .contentsTitle {
        font-size: 60px;
        color: white;
        @include lato;
        font-weight: bold;
        margin-bottom: 12px;
      }

      .contentsContainer {
        margin-left: 32px;
        a {
          text-decoration: none;
        }
        .socialTitle {
          font-size: 44px;
          color: white;
          transition: 400ms;
          &:hover {
            color: $color-secondary;
          }
        }
      }
   }
}
</style>
