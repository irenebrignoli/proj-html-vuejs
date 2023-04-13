<script>
import "@fontsource/lato";
import PageHeader from "./components/PageHeader.vue";
import PageMain from "./components/PageMain.vue";
import PageFooter from "./components/PageFooter.vue";

export default {
  components: {
    PageHeader,
    PageMain,
    PageFooter,
  },
  data() {
    return {
      navLinks: ["home", "about", "projects", "services", "blog", "contact"],
    };
  },
};
</script>

<template>
  <PageHeader :links="navLinks" />
  <PageMain />
  <PageFooter :links="navLinks" />
</template>

<style lang="scss">
@use "./styles/general.scss";
</style>
