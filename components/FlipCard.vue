<template lang="pug">
.cardContainer(@click="toggleActive()")
  .card(:class="activeClass()")
    .side.front
      slot(name="front")
    .side.back
      slot(name="back")
</template>
<script lang="ts">
import Vue from 'vue'
export default Vue.extend({
  name: "FlipCard",
  data() {
    return {
      isActivated: false
    }
  },
  methods: {
    toggleActive() {
      this.isActivated = !this.isActivated;
    },
    activeClass() {
      return this.isActivated ? 'active' : 'inactive';
    },
  }
})
</script>
<style lang="scss" scoped>
@import '../assets/mixin';

@mixin size($x, $y) {
  width: $x;
  height: $y;
}


.cardContainer {
      position: relative;
      width: 360px;
      height: 260px;
      @include mq-down() {
        width: 300px;
        height: 200px;
      }
      margin: 24px;
      perspective: 1000px;
      transition: 0.4s;
   }
  .active {
    transform: translateZ(0px) rotateY(180deg) !important;
    &:after { display: none; }
  }

  .card {
    @include size(100%, 100%);
    display: inline-block;
    cursor: pointer;
    transform-style: preserve-3d;
    transform: translateZ(-100px);
    transition: all 0.4s cubic-bezier(0.165, 0.84, 0.44,1);
    &:after {
      content: '';
      @include size(100%, 100%);
      position: absolute;
      z-index: -1;
      border-radius: 5px;
      box-shadow: 0 14px 50px -4px hsla(0, 0%, 0%, 0.15);
      opacity: 0;
    }
    &:hover {
      transform: translateZ(0px)
    }
    &:hover:after {
      opacity: 1;
    }
  }

  .side {
    @include size(100%, 100%);
    backface-visibility: hidden;
    position: absolute;
    border-radius: 5px;
  }

  .front {
    z-index: 2;
  }

  .back {
    transform: rotateY(180deg);
  }

</style>
