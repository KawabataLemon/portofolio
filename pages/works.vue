<template lang="pug">
.container
  navigation-header(:current-page="'works'")
  section.contents
    .flip-contants
      flip-card
        template(v-slot:front)
          .cardBase
            .imgWrapper
              img(src="../static/cn.png").logo
        template(v-slot:back)
          .cardBase
            .imgWrapper
              img(src="../static/cn.png").backlogo
            .descriptionWrapperSp
              .servicePositionHeader
                h3 Coiney
                span Client Team Manager, iOS Engineer
              span 対面型決済サービス「Coiney」の開発に携わる。heyのSTORESブランドの統合やチームマネジメント、コロナ下でのチームの動き方改善などを行う。現職。
      .descriptionWrapper
        .servicePositionHeader
          h3 Coiney
          span Client Team Manager, iOS Engineer
        span 対面型決済サービス「Coiney」の開発に携わる。heyのSTORESブランドの統合やチームマネジメント、コロナ下でのチームの動き方改善などを行う。現職。
    .flip-contants
      flip-card
        template(v-slot:front)
          .cardBase
            .imgWrapper
              img(src="../static/xb.png").logo
        template(v-slot:back)
          .cardBase
            .imgWrapper
              img(src="../static/xb.png").backlogo
            .descriptionWrapperSp
              .servicePositionHeader
                h3 xenoBrain
                span Web Engineer
              span AIビジネス将来予測形SaaS「xenoBrain」の開発に携わる。新機能開発や、Webフレームワークの導入、開発プロセス改善にも貢献。またWebエンジニアとしてのスキルをみにつける。
      .descriptionWrapper
        .servicePositionHeader
          h3 xenoBrain
          span Web Engineer
        span AIビジネス将来予測形SaaS「xenoBrain」の開発に携わる。新機能開発や、Webフレームワークの導入、開発プロセス改善にも貢献。またWebエンジニアとしてのスキルをみにつける。
    .flip-contants
      flip-card
        template(v-slot:front)
          .cardBase
            .imgWrapper
              img(src="../static/pairs.png").logo
        template(v-slot:back)
          .cardBase
            .imgWrapper
              img(src="../static/pairs.png").backlogo
            .descriptionWrapperSp
              .servicePositionHeader
                h3 Pairs
                span Head Of iOS, Scrum Master
              span マッチングサービスPairsの開発に携わる。チームマネジメント、スクラムマスターの経験を通じてチームとして成果を出す働き方を身につける。チームワーク賞、準MVP賞を受賞。
      .descriptionWrapper
        .servicePositionHeader
          h3 Pairs
          span Head Of iOS, Scrum Master
        span マッチングサービスPairsの開発に携わる。チームマネジメント、スクラムマスターの経験を通じてチームとして成果を出す働き方を身につける。チームワーク賞、準MVP賞を受賞。
    .flip-contants
      flip-card
        template(v-slot:front)
          .cardBase
            .imgWrapper
              img(src="../static/bd.png").logo
        template(v-slot:back)
          .cardBase
            .imgWrapper
              img(src="../static/bd.png").backlogo
            .descriptionWrapperSp
              .servicePositionHeader
                h3 Braindots
                span Game Engineer
              span お絵かき物理ゲーム「Braindots」の開発及び設計を行う。全世界で4000万DLを突破。ゲームエンジンCocos2dx上での物理エンジンの取り扱いや、パフォーマンスチューニングにも貢献。
      .descriptionWrapper
        .servicePositionHeader
          h3 Braindots
          span Game Engineer
        span お絵かき物理ゲーム「Braindots」の開発及び設計を行う。全世界で4000万DLを突破。ゲームエンジンCocos2dx上での物理エンジンの取り扱いや、パフォーマンスチューニングにも貢献。
    .flip-contants
      flip-card
        template(v-slot:front)
          .cardBase
            .imgWrapper
              img(src="../static/bw.png").logo
        template(v-slot:back)
          .cardBase
            .imgWrapper
              img(src="../static/bw.png").backlogo
            .descriptionWrapperSp
              .servicePositionHeader
                h3 Brainwars
                span Game Engineer
              span リアルタイム脳トレバトルゲーム「Brainwars」の開発、運用に関わる。新機能ゲームの実装や、その他サブ機能の実装などを行う
      .descriptionWrapper
        .servicePositionHeader
          h3 Brainwars
          span Game Engineer
        span リアルタイム脳トレバトルゲーム「Brainwars」の開発、運用に関わる。新機能ゲームの実装や、その他サブ機能の実装などを行う
    .flip-contants
      flip-card
        template(v-slot:front)
          .cardBase
            .imgWrapper
              img(src="../static/adstore.png").logo
        template(v-slot:back)
          .cardBase
            .imgWrapper
              img(src="../static/adstore.png").backlogo
            .descriptionWrapperSp
              .servicePositionHeader
                h3 AdStoreTracking
                span Software Engineer
              span 広告効果測定サービスのiOS SDK開発、及びサーバーサイドでの実装を行う。

      .descriptionWrapper
        .servicePositionHeader
          h3 AdStoreTracking
          span Software Engineer
        span 広告効果測定サービスのiOS SDK開発、及びサーバーサイドでの実装を行う。


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
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;

    .flip-contants {
      display: flex;
      flex-direction: row;
      justify-content: center;
      align-content: center;
      .descriptionWrapper {
        z-index:2;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-content: center;
        width: 300px;
        .servicePositionHeader {
          display: flex;
          flex-direction: row;
          justify-content: flex-start;
          align-items: center;
          margin-bottom: 8px;
          padding-bottom: 8px;
          border-bottom: 1px solid black;
          @include lato;
          h3 {
            font-size: 30px;
            margin-right: 12px;
          }
        }
        @include mq-down {
          display: none;
        }
      }
    }
    .cardBase {
      position: relative;
      height: 100%;
      width: 100%;
      padding: 16px;
      display:flex;
      justify-content: center;
      align-items: center;
      background-color: white;
      border-radius: 20px;
      .imgWrapper {
        position: relative;
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
      .descriptionWrapperSp {
        position: absolute;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-content: center;
        width: 280px;
        margin-left: 4px;
        .servicePositionHeader {
          display: flex;
          flex-direction: row;
          justify-content: flex-start;
          align-items: center;
          margin-bottom: 8px;
          padding-bottom: 8px;
          border-bottom: 1px solid black;
          @include lato;
          h3 {
            font-size: 20px;
            margin-right: 12px;
          }
        }
        @include mq-up {
          display: none;
        }
      }
    }
  }
}

</style>
