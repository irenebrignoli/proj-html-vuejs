<script>
import ConsultantsCard from "../components/ConsultantsCard.vue";
import Subheading from "./Subheading.vue";
import CtaGreen from "./CtaGreen.vue";
import ProjectCard from "./PorjectCard.vue";
import SubheadingVariant from "./SubheadingVariant.vue";
import TestimonialCard from "./TestimonialCard.vue";
import BlogCard from "./BlogCard.vue";

export default {
  name: "PageMain",
  components: {
    ConsultantsCard,
    Subheading,
    SubheadingVariant,
    CtaGreen,
    ProjectCard,
    TestimonialCard,
    BlogCard,
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
      projects: [
        {
          image: "p1",
          title: "Dry products",
          hover: false,
        },
        {
          image: "p2",
          title: "Sponsorship",
          hover: false,
        },
        {
          image: "p3",
          title: "Vizeon",
          hover: false,
        },
      ],
      testimonials: [
        {
          image: "t1",
          name: "Vera Duncan",
          hover: false,
        },
        {
          image: "t2",
          name: "Tom British",
          hover: false,
        },
        {
          image: "t3",
          name: "Pablo Escobar",
          hover: false,
        },
      ],
      blogs: [
        {
          image: "blog1",
          date: "july 4, 2019",
          writer: "paul",
          title: "Canadian Consulting Firm acquired by UK Giant",
          text: "When, while lovely valley teems with vapour around meand eridian sun strikes the upper impenetrable foliage of my trees, and but a",
        },
        {
          image: "blog2",
          date: "april 10, 2022",
          writer: "jennifer",
          title: "Italins acquire UK Giant",
          text: "When, while lovely valley teems with vapour around meand eridian sun strikes the upper impenetrable foliage of my trees, and but a",
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

  <!-- BACKGROUND BLUE -->
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

    <!-- project section-->
    <section id="project">
      <div class="container">
        <div class="d-flex justify-content-between align-items-center">
          <div>
            <Subheading subtitle="Project" />
            <h3 class="main_title_repeat">
              Our expert trusted consultants<br />help clients
            </h3>
          </div>

          <div class="arrows d-flex gap-2">
            <div class="arrow"><i class="fa-solid fa-arrow-left"></i></div>
            <div class="arrow"><i class="fa-solid fa-arrow-right"></i></div>
          </div>
        </div>

        <div class="row mt-5">
          <div v-for="(project, i) in projects" :key="i" class="col">
            <ProjectCard :project="project" />
          </div>
        </div>
      </div>
    </section>

    <!-- testimonial section -->
    <section id="testimonial">
      <div class="container">
        <SubheadingVariant subtitle="Testimonial" />
        <h3 class="main_title_repeat text-end">
          What's the customer say<br />about our work
        </h3>
      </div>
      <div class="d-flex justify-content-end">
        <div class="customers row mt-5">
          <div v-for="(testimonial, i) in testimonials" :key="i" class="col">
            <TestimonialCard :testimonial="testimonial" />
          </div>
        </div>
      </div>
    </section>

    <!-- blog section -->
    <section id="blog">
      <div class="container">
        <div class="d-flex justify-content-between align-items-center">
          <div>
            <Subheading subtitle="Blog" />
            <h3 class="main_title_repeat">The Recent news you must read it</h3>
          </div>
          <button class="ms_btn ms_btn_green">View all</button>
        </div>

        <div class="row mt-5 gap-4">
          <div v-for="(blog, i) in blogs" :key="i" class="col">
            <BlogCard :blog="blog" />
          </div>
        </div>
      </div>
    </section>

    <!-- boh -->
    <section id="boh"></section>
  </div>
</template>

<style lang="scss" scoped>
@use "../styles/partials/variables" as *;
@use "../styles/partials/buttons" as *;

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

  #project {
    margin-top: 10rem;

    .arrow {
      width: 3rem;
      height: 3rem;
      background-color: $bg_arrows;
      text-align: center;

      i {
        color: $text_dirty_white;
        font-size: 0.8rem;
        line-height: 3rem;
      }
    }
  }

  #testimonial {
    margin-top: 10rem;
    .customers {
      height: 18rem;
      background-color: $bg_white;
      width: 90%;

      .col {
        padding: 0;
      }
    }
  }

  #blog {
    margin: 10rem 0;

    .col {
      padding: 0;
    }
  }

  #boh {
    height: 60rem;
  }
}
</style>
