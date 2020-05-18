<template lang="pug">
section.bottom
  .bottomNavigation
    .navBarContainer
      a(href="/").navBarItem(:class="isCurrentPage('about') ? 'selected' : ''")
        span about
      a(href="/works").navBarItem(:class="isCurrentPage('works') ? 'selected' : ''")
        span works
      a(href="/contact").navBarItem(:class="isCurrentPage('contact') ? 'selected' : ''")
        span contact
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
.bottom {
  height: 100px;
  .bottomNavigation {
    @include mq-down() {
      display:flex;
    }

    overflow: hidden;
    position: fixed;
    bottom: 0;
    width: 100%;
    display: none;
    align-content: center;
    justify-content: center;
    background: $color-accent;
    border-radius: 50px 0 0 0;
    .navBarContainer {
      height: 60px;
      background: $color-accent;
      min-width: 320px;
      max-width: 480px;
      display: flex;
      justify-content: space-between;
      align-items: center;
      .navBarItem {
        @include lato;
        text-decoration: none;
        font-size: 24px;
        font-weight: bold;
        color: white;
        &.selected {
          color: $color-accent-secondary;
        }
      }
    }
  }
}

</style>
