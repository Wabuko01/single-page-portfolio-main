<template>
  <div>
    <IntroComponent />
    <LanguagesComponent />
    <ProjectsComponent />
    <ContactComponent />
    <FooterComponentVue />
  </div>
</template>
<script>
import ContactComponent from "@/components/ContactComponent.vue";
import FooterComponentVue from "@/components/FooterComponent.vue";
import IntroComponent from "@/components/IntroComponent.vue";
import LanguagesComponent from "@/components/LanguagesComponent.vue";
import ProjectsComponent from "@/components/ProjectsComponent.vue";

export default {
  components: {
    ContactComponent,
    IntroComponent,
    LanguagesComponent,
    ProjectsComponent,
    FooterComponentVue,
  },
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
<style lang='scss' scoped>
</style>