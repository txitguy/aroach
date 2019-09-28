<template lang="pug">
  .experience
    section#experience.bg-white.py-5
      .container
        .row
          .col-12
            .title
              h3 Experience
              span My work experience
        .row
          .col-12
            ul.timeline()
              li(v-for="(job, i) in jobs", v-show='i < 3 || jobsExpanded')
                .card(:class="{'bg-light': (i%2)}")
                  .card-body
                    h5.card-title {{job.title}}
                      .span.float-right.text-muted.tx-16 {{job.startDate}} - {{job.endDate}}
                    h6.card-subtitle.mb-2.text-muted {{job.company}}
                    p.card-text {{job.description}}
              li
                a(href="javascript:void(0)", @click.prevent="toggleExpand") Show
                  span(v-if='jobsExpanded')  Less
                  span(v-else)  More
</template>

<style lang="scss" scoped>
@import "../scss/theme.scss";
ul.timeline {
  list-style-type: none;
  position: relative;
  clear: both;

  &:before {
    content: " ";
    background: #d4d9df;
    display: inline-block;
    position: absolute;
    left: 29px;
    width: 2px;
    height: 100%;
    z-index: 99;
  }

  & > li {
    margin: 20px 0;
    padding-left: 20px;

    &:before {
      content: " ";
      background: white;
      display: inline-block;
      position: absolute;
      border-radius: 50%;
      border: 3px solid $primary;
      left: 20px;
      width: 20px;
      height: 20px;
      z-index: 99;
    }
  }
}
</style>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";
import JobModel from "@/models/job";

export default class Experience extends Vue {
  jobsToShow: number = 3;
  jobsExpanded: boolean = false;
  jobs: JobModel[] = [
    {
      title: "Engineering Manager",
      company: "Scotsman Guide Media",
      description:
        "Designed and developed web applications and services for lead generation and marketing. Developed front-end CLI tools that allowed designers to rapidly develop prototypes. Built front-end framework built from Vue.js to help create an SPA website. Provided dev-ops support and designed developer workflow and deployment strategies",
      startDate: "02/2018",
      endDate: "Current"
    },
    {
      title: "Sr Software Engineer",
      company: "Market Leader / Zillow",
      description:
        "Acted in a lead developer capacity on several projects, including developing our hybrid mobile application using AngularJS and Ionic. I saw this project through from conception in a decision-making role, while also leading developers and setting project standards. I was responsible for creating coding standards standards, functional specs, design documents, and other documentation. I acted as a mentor and helped other engineers learn the technology layers",
      startDate: "09/2014",
      endDate: "02/2018"
    },
    {
      title: "Sr Software Engineer",
      company: "Front Gate Tickets",
      description:
        "Assisted in the development of a new AngularJS project while working in a leadership and decision-making role to assist staff working concerts and other major events. Participated and gave guidance during the conceptualization stage as well as provided insight into problem areas. Developed and implemented coding standards and a code review process to enforce such standards.",
      startDate: "07/2013",
      endDate: "03/2014"
    },
    {
      title: "Software Engineer",
      company: "Home Improvement Leads",
      description:
        "Worked independently as well as in a mentoring capacity to junior developers, I was responsible for development of lead generation websites and tools. I initially solely developed, and later acted as lead developer, for a lead-buying platform used by contractors using CakePHP. I worked directly with upper management to provide insight into technological solutions for known problems.",
      startDate: "03/2012",
      endDate: "07/2013"
    },
    {
      title: "CEO",
      company: "Sudo Media Group",
      description:
        "Developed email marketing technologies to assist in mass outgoing email-marketing campaigns. I was an owner and lead developer of the company and provided the leadership and knowledge to assist developers in a state of the art automated email solution.",
      startDate: "01/2011",
      endDate: "03/2012"
    },
    {
      title: "Email Marketing Director",
      company: "eComLeads, LLC",
      description:
        "Acted in a leadership role in leading successful email marketing campaigns. I lead a team of developers, designers, and others to create email technologies. I was responsible for the development of a system that allowed us to manage website themes on hundreds of our domains.",
      startDate: "03/2009",
      endDate: "10/2011"
    },
    {
      title: "Owner",
      company: "Texas IT Consulting & Services",
      description:
        "As an independent contractor, I specialized in medical technology and compliance. I managed a team of developers in India in the creation of an electronic medical records solution, primarily targeted at use from Cardiologists and Radiologists. I lead the development of tools that allow clients to view and measure DICOM images from MRI equipment.",
      startDate: "02/2007",
      endDate: "03/2009"
    }
  ];

  toggleExpand() {
    this.jobsExpanded = !this.jobsExpanded;
    this.$forceUpdate();

    if (!this.jobsExpanded) {
      document.querySelector("#experience")!.scrollIntoView({
        behavior: "smooth"
      });
    }
  }
}
</script>
