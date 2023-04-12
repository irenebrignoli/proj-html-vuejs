<script>
import ConsultantsCard from "../components/ConsultantsCard.vue";
import Subheading from "./Subheading.vue";
import CtaGreen from "./CtaGreen.vue";

export default {
  name: "PageMain",
  components: {
    ConsultantsCard,
    Subheading,
    CtaGreen,
  },
  data() {
    return {
      consultants: [
        {
          title: "Statistical consulting",
          icon: "fa-chart-line",
        },
        {
          title: "Digital consulting",
          icon: "fa-bullhorn",
        },
        {
          title: "Banking consulting",
          icon: "fa-piggy-bank",
        },
        {
          title: "Enterprise consulting",
          icon: "fa-bullseye",
        },
      ],
    };
  },
};
</script>

<template>
  <!-- consultants section -->
  <section id="consultants">
    <div class="row justify-content-center">
      <div class="col-8">
        <h5 class="main_title flex-shrink-0">Our consultants con help you</h5>
        <div class="row flex-wrap justify-content-between gy-5">
          <div v-for="(consultant, i) in consultants" :key="i" class="col-5">
            <ConsultantsCard :consultant="consultant" />
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- background blue -->
  <div class="blue_area">
    <!-- about us section -->
    <section id="about_us">
      <div class="row h-100">
        <div class="col-7 red_img_col"></div>
        <div class="col-5">
          <div class="text_box">
            <Subheading subtitle="About us" />
            <h2 class="main_title mt-3">We make your<br />strategy work</h2>
            <p class="text_section mt-3">
              When, while lovely valley teems with vapour around meanderidian
              sun strikes the upper impenetrable foliage of my trees, and but a
              thousand unknown plants are noticed when I hear the buzz of the
              little world among the stalks,and grow familiar indescribable
              forms of the insects .and flies, then I feel the presence of the
              Almighty.
            </p>
          </div>
        </div>
      </div>
    </section>

    <!-- Cta green-->
    <CtaGreen />
  </div>
</template>

<style lang="scss" scoped>
@use "../styles/partials/variables" as *;

#consultants {
  margin: 5rem 0;
  color: $text_dark_gray;
  position: relative;

  .main_title {
    margin-bottom: 4.5rem;
    font-size: 1.4rem;

    &:after {
      content: "";
      background-color: $bg_darker_green;
      height: 2.5px;
      width: 55%;
      position: absolute;
      right: 0;
      top: 1rem;
    }
  }
}

.blue_area {
  background-color: $bg_darkblue;

  #about_us {
    height: 40rem;
    .red_img_col {
      background-image: url("../assets/images/business-people-working-together-on-project-and-5FHSKBL.jpg");
    }

    .text_box {
      margin: 14rem 0 0 3rem;
      width: 60%;

      .main_title {
        color: $text-white;
        font-size: 2.5rem;
      }

      .text_section {
        color: $text_gray;
      }
    }
  }
}
</style>
