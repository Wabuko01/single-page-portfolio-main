<template>
  <div class="lang-wrapper">
    <div class="lang">
      <h3>HTML</h3>
      <p>4 Years Experience</p>
    </div>
    <div class="lang">
      <h3>CSS</h3>
      <p>4 Years Experience</p>
    </div>
    <div class="lang">
      <h3>JavaScript</h3>
      <p>4 Years Experience</p>
    </div>
    <div class="lang">
      <h3>Accessibility</h3>
      <p>4 Years Experience</p>
    </div>
    <div class="lang">
      <h3>React</h3>
      <p>3 Years Experience</p>
    </div>
    <div class="lang">
      <h3>Sass</h3>
      <p>3 Years Experience</p>
    </div>
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

<style lang='css' scoped>
.lang-wrapper {
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  background-color: var(--main-bg-color);
  padding: 3rem var(--padding-x);
  width: auto;
}
.lang-wrapper .lang {
  display: flex;
  flex-direction: column;
  flex-basis: 45%;
  padding: 1rem;
}
.lang-wrapper .lang h3 {
  font-size: var(--l-font);
  font-family: var(--font-family-main);
  color: var(--white);
  font-weight: 700;
  letter-spacing: var(--m-char-spacing);
  line-height: var(--m-line-height);
  padding: 1rem 0;
}
.lang-wrapper .lang p {
  font-size: var(--s-font);
  font-family: var(--font-family-main);
  color: var(--light-gray);
  font-weight: 500;
  line-height: var(--m-line-height);
}
@media (max-width: 768px) {
  .lang-wrapper .lang h3 {
    font-size: 35px;
  }
  .lang-wrapper .lang {
    flex-basis: 40%;
  }
}
@media (max-width: 450px) {
  .lang-wrapper .lang {
    flex-basis: 100%;
    align-items: center;
  }
}
</style>
