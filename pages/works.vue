<template lang="pug">
  .container
    navigation-header(:current-page="'works'")
    section.contents
    navigation-footer(:current-page="'works'")
</template>

<script lang="ts">
import Vue from 'vue'
import NavigationHeader from '../components/NavigationHeader.vue';
import NavigationFooter from '../components/NavigationFooter.vue';
export default Vue.extend({
  name: "works",
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

   .contents{}
}
</style>
