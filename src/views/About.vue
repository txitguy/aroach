<template lang="pug">
  .about
    section#about.bg-white.py-5
      .container
        .row
          .col-12
            .title
              h3 About me
              span A bit of information about me
        .row.clearfix
          .col-lg-4.mb-5.mb-lg-0
            img.img-fluid(src="/images/me.jpg", alt="Mark Roach")
          .col-lg-8
            h4 Mark Roach
            h5.text-secondary.text-nowrap {{getTypewriterText()}}&nbsp;
            p I'm a self-taught Software Engineer with over 20 years of experience, over 10 of which are professional. While a lot of my career focus has been in development, I have also become an expert in UI/UX design, marketing, and business management.
            p I have a proven track record with software development and project management, ensuring products are designed and implemented with strict standards, while also providing accurate time and budget estimates. I have experience with various project management softwares, including Atlassian, which allow me to quickly engage development teams and ensure they are on-track and successful.
            p Throughout my vast development career I have spent a lot of timing focusing on UI/UX design with the various websites and applications I have developed.  Through rigorous testing, user surveys, and research I have developed the skills to design world-class applications that provide users with an excellent experience.
            p Starting early on in my career I was involved in digital marketing campaigns of various nature.  From PPC ad campaigns to affiliate networks and SEO, I have developed the technical expertise to launch and manage high producing marketing campaigns.

    section.bg-light.py-5
      .container
        .row
          .col-12
            h5.text-dark Some of my skills
        .row.mt-4 
          .col-lg-6.col-xl-3
            ul
              li.font-weight-bold Management
              li Leadership
              li Project Management
              li Team Building
              li Mentoring
              li Career Development
          .col-lg-6.col-xl-3
            ul
              li.font-weight-bold Development
              li .NET Core
              li PHP
              li Python
              li SQL
              li Mobile Apps
          .col-lg-6.col-xl-3
            ul
              li.font-weight-bold Design
              li UI/UX
              li CSS3
              li HTML5
              li JavaScript
              li Responsive Web
          .col-lg-6.col-xl-3
            ul
              li.font-weight-bold Marketing
              li SEO
              li Email Marketing
              li Affiliate Marketing
              li PPC Ad Networks
              li Business Intelligence

</template>

<script lang="ts">
import { Vue, Component } from "vue-property-decorator";
import Typewriter from "@/components/Typewriter.vue";
import Home from "./Home.vue";

@Component
export default class About extends Vue {
  getTypewriterText: Function = (this.$parent as Home).getTypewriterText;
}
</script>
