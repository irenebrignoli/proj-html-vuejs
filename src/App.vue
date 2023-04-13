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
      navLinks: ["Home", "About", "Projects", "Services", "Blog", "Contact"],
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
