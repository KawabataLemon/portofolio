<template lang="pug">
section.header
  .title
    span Kawabata Kazuki
  .navigation
    a(href="/")
      span.menuItem(:class=" isCurrentPage('about') ? 'selected' : ''") about
    a(href="/works")
      span.menuItem(:class=" isCurrentPage('works') ? 'selected' : ''") works
    a(href="/contact")
      span.menuItem(:class=" isCurrentPage('contact') ? 'selected' : ''") contact

</template>
<script lang="ts">
import Vue from 'vue'
export default Vue.extend({
  props: {
    currentPage: {
      type: String,
      default: 'about'
    }
  },
  methods: {
    isCurrentPage(value: String): boolean {
      return value == this.currentPage;
    }
  }
})
</script>
<style lang="scss" scoped>
@import '../assets/main';
@import '../assets/mixin';

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

      @include mq-down() {
        font-size: 30px;
      }
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
</style>
