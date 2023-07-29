<template>
  <div class="intro-wrapper">
    <header>
      <div class="name">
        <p>Wabuko</p>
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
    </header>

    <div class="intro">
      <div class="greetings">
        <img src="../assets/images/profile-pic.jpg" alt="" class="img" />
        <h1>
          Nice to meet you! <br />
          I'm <span><a href="#"> Wabuko Aggrey</a>. </span>
        </h1>
        <p>
          Based in the UK, I'm a front-end developer passionate about building
          accessible web apps that users love.
        </p>
      </div>
      <div class="contact"><h2>CONTACT ME</h2></div>
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
<style scoped lang="css">
.intro-wrapper {
  display: flex;
  flex-direction: column;
  margin: 0 var(--padding-x);
  min-height: 720px;
  padding-bottom: 2rem;
  border-bottom: 1px solid var(--white);
}
.intro-wrapper header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 2rem 0;
}
.intro-wrapper header .name {
  background: none;
  z-index: 2;
}
.intro-wrapper header .name p {
  font-size: var(--m-font);
  font-family: var(--font-family-main);
  color: var(--white);
  font-weight: 500;
  letter-spacing: var(--m-char-spacing);
  line-height: var(--m-line-height);
  text-decoration: none;
  z-index: 2;
  background: none;
}
.intro-wrapper header .social-links {
  display: flex;
  z-index: 2;
  flex-direction: row;
  gap: 2rem;
  background: none;
}
.intro-wrapper header .social-links a,
.intro-wrapper header .social-links .front-end-mentor svg path {
  color: var(--white);
  text-decoration: none;
  font-size: var(--m-font);
  font-family: var(--font-family-main);
  background: none;
}
.intro-wrapper header .social-links svg {
  background: none;
}

.intro-wrapper header .social-links a:hover,
.intro-wrapper header .social-links .front-end-mentor:hover svg path {
  color: var(--green-color);
  fill: var(--green-color);
}
.intro-wrapper .intro {
  display: flex;
  flex-direction: column;
}
.intro-wrapper .intro .greetings {
  display: flex;
  flex-direction: column;
  padding: 5rem 0;
  min-height: 303px;
  gap: 2rem;
  justify-content: space-between;
}
.intro-wrapper .intro h1 {
  font-size: var(--xl-font);
  font-family: var(--font-family-main);
  z-index: 2;
  background: none;
  color: var(--white);
  font-weight: 700;
  width: fit-content;
  letter-spacing: var(--xl-char-spacing);
  line-height: var(--xl-line-height);
}
.intro-wrapper .intro h1 span {
  background: none;
  z-index: 2;
}
.intro-wrapper .intro h1 span a {
  background: none;
  z-index: 2;
  color: var(--white);
  text-decoration: underline var(--green-color);
}
.intro-wrapper .intro p {
  font-size: var(--s-font);
  font-family: var(--font-family-main);
  color: var(--light-gray);
  z-index: 2;
  font-weight: 400;
  background: none;
  line-height: var(--s-line-height);
  max-width: 500px;
}

.intro-wrapper .intro .contact {
  padding-bottom: 100px;
}
.intro-wrapper .intro h2 {
  position: relative;
  font-size: var(--s-font);
  font-family: var(--font-family-main);
  color: var(--white);
  font-weight: 500;
  line-height: var(--s-line-height);
  border-bottom: 0.2rem solid var(--green-color);
  width: fit-content;
  padding-bottom: 0.5rem;
}
.intro-wrapper .intro h2:hover {
  color: var(--green-color);
}
.intro-wrapper .intro .img {
  position: absolute;
  right: 3rem;
  z-index: 1;
  top: 0;
  width: 445px;
  height: 720px;
}
@media screen and (max-width: 900px) {
  .intro-wrapper .intro h1 {
    font-size: 77px;
  }
}
@media screen and (max-width: 768px) {
  .intro-wrapper header .intro {
    max-width: 445px;
  }

  .intro-wrapper .intro .img {
    width: 322px;
    height: 600px;
    object-fit: cover;
  }
  .intro-wrapper .intro h1 {
    font-size: 65px;
  }
}

@media screen and (max-width: 450px) {
  .intro-wrapper {
    margin: 1rem;
  }
  .intro-wrapper header {
    flex-direction: column;
    align-items: center;
    gap: 2rem;
  }
  .intro-wrapper .intro {
    display: flex;
    flex-direction: column;
  }
  .intro-wrapper .intro .greetings {
    display: flex;
    flex-direction: column;
    margin: auto;
    padding: 0;
    min-height: 303px;
    gap: 2rem;
    align-items: center;
  }

  .intro-wrapper .intro .img {
    width: 175px;
    position: inherit;
    height: 383px;
    object-fit: cover;
  }
  .intro-wrapper .intro .greetings h1 {
    font-size: 40px;
    line-height: var(--l-line-height);
    letter-spacing: -1.14px;
    text-align: center;
  }
  .intro-wrapper .intro p {
    font-size: 18px;
    line-height: 30px;
    padding: 2rem 0;
  }
  .intro-wrapper .intro h2 {
    font-size: 18px;
  }
}
</style>