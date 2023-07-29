<template>
  <div class="contact">
    <div class="contact-wrapper">
      <div class="left">
        <h1>Contact</h1>
        <p>
          I would love to hear about your project and how I could help. Please
          fill in the form, and I'll get back to you as soon as possible.
        </p>
      </div>
      <div class="right">
        <form @submit.prevent="">
          <div class="form-group">
            <input
              type="text"
              id="name"
              placeholder="NAME"
              @input="validateName"
              v-model="name"
              :class="{ 'invalid-field': invalidName }"
            />
            <p v-if="invalidName" class="error">{{ nameError }}</p>
          </div>
          <div class="form-group">
            <input
              type="email"
              id="email"
              placeholder="EMAIL"
              @input="validateEmail"
              v-model="email"
              :class="{ 'invalid-field': invalidEmail }"
            />
            <p v-if="invalidEmail" class="error">{{ emailError }}</p>
          </div>
          <div class="form-group">
            <textarea
              id="message"
              placeholder="MESSAGE"
              @input="validateMessage"
              v-model="message"
              :class="{ 'invalid-field': invalidMessage }"
            ></textarea>
            <p v-if="invalidMessage" class="error">{{ messageError }}</p>
          </div>
          <button type="submit">SEND MESSAGE</button>
        </form>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  components: {},
  props: {},
  data() {
    return {
      name: "",
      email: "",
      message: "",
      invalidName: false,
      invalidEmail: false,
      invalidMessage: false,
      nameError: "",
      emailError: "",
      messageError: "",
    };
  },
  created() {},
  methods: {
    validateName() {
      if (this.name.length == 0) {
        this.invalidName = true;
        this.nameError = "Name is required";
      } else if (this.name.length < 3) {
        this.invalidName = true;
        this.nameError = "Name must be at least 3 characters long";
      } else {
        this.invalidName = false;
        this.nameError = "";
      }
    },
    validateEmail() {
      if (this.email.length == 0) {
        this.invalidEmail = true;
        this.emailError = "Email is required";
      } else if (!this.email.includes("@")) {
        this.invalidEmail = true;
        this.emailError = "Email must be valid";
      } else {
        this.invalidEmail = false;
        this.emailError = "";
      }
    },
    validateMessage() {
      if (this.message.length == 0) {
        this.invalidMessage = true;
        this.messageError = "Message is required";
      } else if (this.message.length < 5) {
        this.invalidMessage = true;
        this.messageError = "Message must be at least 10 characters long";
      } else {
        this.invalidMessage = false;
        this.messageError = "";
      }
    },
  },
  mounted() {},
  computed: {},
  watch: {
    name() {
      this.validateName();
    },
    email() {
      this.validateEmail();
    },
    message() {
      this.validateMessage();
    },
  },
};
</script>

<style lang='css' scoped>
.contact {
  padding: 0 var(--padding-x);
  background-color: var(--dark-gray);
  width: auto;
  position: relative;
}
.contact-wrapper {
  display: flex;
  flex-wrap: wrap;
  flex-direction: row;
  background-color: var(--dark-gray);
  border-bottom: 1px solid var(--white);
  justify-content: space-between;
  padding: 3rem 0;
  position: relative;
}
.contact-wrapper .left {
  display: flex;
  flex-basis: 45%;
  background-color: var(--dark-gray);
  flex-direction: column;
  padding: 2rem 0;
}
.contact-wrapper .left h1 {
  font-size: var(--xl-font);
  font-family: var(--font-family-main);
  background-color: var(--dark-gray);
  color: var(--white);
  font-weight: 700;
  letter-spacing: var(--xl-char-spacing);
  line-height: var(--xl-line-height);
  padding-bottom: 2rem;
}
.contact-wrapper .left p {
  font-size: var(--s-font);
  font-family: var(--font-family-main);
  background-color: var(--dark-gray);
  color: var(--light-gray);
  font-weight: 500;
  line-height: var(--s-line-height);
  padding: 1rem 0;
}
.contact-wrapper .right {
  display: flex;
  flex-basis: 45%;
  background-color: var(--dark-gray);
  position: relative;
  flex-direction: column;
  padding: 2rem 0;
}
.contact-wrapper .right form {
  display: flex;
  flex-direction: column;
  position: relative;
  background-color: var(--dark-gray);
  gap: 1rem;
}
.contact-wrapper .right form .form-group {
  position: relative;
  display: flex;
  background-color: var(--dark-gray);
  flex-direction: column;
  gap: 0.5rem;
}

.contact-wrapper .right form .form-group input,
.contact-wrapper .right form .form-group textarea {
  background-color: var(--dark-gray);
  border: none;
  position: relative;
  padding: 1rem 1.5rem;
  font-size: var(--s-font);
  font-family: var(--font-family-main);
  color: var(--white);
  font-weight: 500;
  letter-spacing: var(--m-char-spacing);
  line-height: var(--m-line-height);
  border-bottom: 1px solid var(--white);
  text-transform: uppercase;
}
.contact-wrapper .right form .form-group input:focus,
.contact-wrapper .right form .form-group textarea:focus {
  outline: none;
  border-bottom: 2px solid var(--green-color);
}
.contact-wrapper .right form .form-group textarea {
  resize: none;
  height: 7rem;
}

.contact-wrapper .right form button {
  background-color: var(--dark-gray);
  border: none;
  display: flex;
  border-bottom: 2px solid var(--green-color);
  padding: 0.5rem;
  margin: auto 0 1rem auto;
  font-size: var(--s-font);
  font-family: var(--font-family-main);
  color: var(--white);
  font-weight: 500;
  letter-spacing: var(--m-char-spacing);
  line-height: var(--m-line-height);
}
.contact-wrapper .right form button:hover {
  cursor: pointer;
  color: var(--green-color);
}
.contact-wrapper .right form .error {
  font-size: var(--xs-font);
  font-family: var(--font-family-main);
  color: var(--error-color);
  font-weight: 100;
  background: none;
  letter-spacing: var(--xs-char-spacing);
  line-height: var(--xs-line-height);
  text-align: right;
}

.invalid-field {
  border-bottom: 1px solid var(--error-color) !important;
}
.contact-wrapper .right form .error::before {
  content: "!";
  width: 2rem;
  height: 2rem;
  font-size: 1.5rem;
  border-radius: 50%;
  outline: 1px solid currentColor;
  position: absolute;
  right: 1px;
  top: 0.5rem;
  display: flex;
  justify-content: center;
  align-items: center;
}
@media screen and (max-width: 768px) {
  .contact-wrapper {
    flex-direction: column;
    padding: 3rem 0;
  }
  .contact-wrapper .left h1 {
    font-size: var(--l-font);
  }
}
</style>