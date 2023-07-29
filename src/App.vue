<template>
  <div id="app">
    <router-view />
  </div>
</template>
<script>
export default {
  components: {},
  props: {},
  data() {
    return {};
  },
  created() {},
  methods: {},
  mounted() {},
};
</script>
<style scoped>
</style>
<style lang='css'>
* {
  margin: 0;
  padding: 0;
  background-color: var(--main-bg-color);
}

:root {
  --main-bg-color: #151515;
  --green-color: #4ee1a0;
  --dark-gray: #242424;
  --light-gray: #d9d9d9;
  --white: #ffffff;
  --error-color: #f46262;
  --xl-font: 88px;
  --font-family-main: "Space Grotesk", sans-serif;
  --xl-char-spacing: -2.5px;
  --xl-line-height: 88px;
  --l-font: 48px;
  --l-line-height: 56px;
  --l-char-spacing: -1.5px;
  --m-font: 24px;
  --m-line-height: 32px;
  --s-font: 18px;
  --s-line-height: 28px;
  --xs-font: 16px;
  --xs-line-height: 24px;
  --xs-char-spacing: 0.5px;
  /*  */
  --padding-x: 3rem;
}
#app {
  background-image: url(./assets/images/pattern-circle.svg);
  background-repeat: no-repeat;
  background-position: 84vw 67.5vw;
}
</style>