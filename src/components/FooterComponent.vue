<template>
  <div class="footer">
    <footer>
      <div class="name">
        <a href="#" target="_blank">Wabuko</a>
      </div>
      <div class="social-links">
        <a href="#">
          <font-awesome-icon :icon="['fab', 'github']" />
        </a>
        <a href="#" class="front-end-mentor" target="_blank">
          <svg
            xmlns="http://www.w3.org/2000/svg"
            viewBox="0 0 26 23"
            width="26"
            height="23"
            aria-hidden="true"
          >
            <path
              fill="#FFF"
              d="M13.084.23a.751.751 0 0 0-.736.75v14.267a.75.75 0 1 0 1.5 0V.98a.75.75 0 0 0-.763-.75ZM24.44 4.504a.752.752 0 0 0-.284.064l-6.44 2.875a.752.752 0 0 0 0 1.37l6.44 2.884a.75.75 0 0 0 .612-1.369L19.861 8.13l4.907-2.191a.753.753 0 0 0 .38-.99.752.752 0 0 0-.708-.444ZM1.371 9.663a.752.752 0 0 0-.74.938C2.41 17.447 8.603 22.23 15.685 22.23a.75.75 0 1 0 0-1.501A14.053 14.053 0 0 1 2.083 10.225a.75.75 0 0 0-.712-.561v-.001Z"
            />
          </svg>
        </a>
        <a href="#">
          <font-awesome-icon :icon="['fab', 'linkedin']" />
        </a>
        <a href="#">
          <font-awesome-icon :icon="['fab', 'twitter']" />
        </a>
      </div>
    </footer>
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
.footer {
  background-color: var(--dark-gray);
  padding: 0 var(--padding-x);
  width: auto;
}
.footer footer {
  display: flex;
  justify-content: space-between;
  align-items: center;
  background-color: var(--dark-gray);
  padding: 2rem 0;
}
.footer footer .name {
  background-color: var(--dark-gray);
}
.footer footer .name a {
  font-size: var(--m-font);
  font-family: var(--font-family-main);
  color: var(--white);
  background-color: var(--dark-gray);
  font-weight: 500;
  letter-spacing: var(--m-char-spacing);
  line-height: var(--m-line-height);
  text-decoration: none;
}
.footer footer .social-links {
  display: flex;
  flex-direction: row;
  background-color: var(--dark-gray);
  gap: 2rem;
}
.footer footer .social-links a,
.footer footer .social-links .front-end-mentor svg path {
  color: var(--white);
  background-color: var(--dark-gray);
  text-decoration: none;
  font-size: var(--m-font);
  font-family: var(--font-family-main);
}
.footer footer .social-links a svg,
.footer footer .social-links .front-end-mentor svg {
  width: 1.5rem;
  height: 1.5rem;
  background-color: var(--dark-gray);
}
.footer footer .social-links a:hover,
.footer footer .social-links .front-end-mentor:hover svg path {
  color: var(--green-color);
  fill: var(--green-color);
}
@media screen and (max-width: 450px) {
  .footer footer {
    flex-direction: column;
    gap: 1rem;
  }
}
</style>