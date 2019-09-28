<template lang="pug">
  .home
    section#home
      .overlay
        .photo
        h3.mt-3
          | Mark
          span  Roach
        Typewriter.text-white.tx-24(:toRotate="toRotate", base="I'm a ", ref="typewriter")

    section#about.bg-white.py-5
      .container
        .row
          .col-12
            .title
              h3 About me
              span Main information about me
        .row.clearfix
          .col-lg-4.mb-5.mb-lg-0
            img.img-fluid(src="/images/me.jpg", alt="Mark Roach")
          .col-lg-8
            h4 I'm Mark Roach and a
              span.text-secondary.text-nowrap  {{getTypewriterText()}}
            p Hi! I'm 
              span.text-secondary  Mark Roach
              | . Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
            p Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
            p Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
    section.bg-light.py-5
      .container
        .row
          .col-12
            h5.text-dark Some of my skills
        .row.mt-4
          .col-lg-4
            ul
              li.font-weight-bold Management
              li Leadership
              li Project Management
              li Team Building
              li Mentoring
              li Career Development
          .col-lg-4
            ul
              li.font-weight-bold Development
              li .NET Core
              li PHP
              li Python
              li SQL
              li Mobile Apps
          .col-lg-4
            ul
              li.font-weight-bold Design
              li UI/UX
              li CSS3
              li HTML5
              li JavaScript
              li Responsive Web
    section#quote-leader.quote
      .overlay
        .container
          h3
            span
              i.icon.ion-md-quote
          .py-3.px-5.mx-5.text-white
            p.font-weight-bold.tx-24 "Mark is a strong, organized manager who has high standards but also consistently demonstrates compassion for his co-workers."
            p.pt-3 - Kevin Britton-Simmons, CEO of Scotsman Guide Media
    section#experience.bg-white.py-5
      .container
        .row
          .col-12
            .title
              h3 Experience
              span My work experience
        .row
          .col-12
            ul.timeline
              li
                .card
                  .card-body
                    h5.card-title Engineering Manager
                      .span.float-right.text-muted.tx-16 02/2018 - Current
                    h6.card-subtitle.mb-2.text-muted Scotsman Guide Media
                    p.card-text Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
                    p.card-text Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
              li
                .card
                  .card-body
                    h5.card-title Sr Software Engineer
                      .span.float-right.text-muted.tx-16 02/2018 - Current
                    h6.card-subtitle.mb-2.text-muted Market Leader / Zillow
                    p.card-text Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
                    p.card-text Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
              li
                .card
                  .card-body
                    h5.card-title Software Engineer
                      .span.float-right.text-muted.tx-16 02/2018 - Current
                    h6.card-subtitle.mb-2.text-muted Front Gate Tickets
                    p.card-text Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
                    p.card-text Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
              li
                a(href="#") View More
    section#quote-dev.quote
      .overlay
        .container
          h3
            span
              i.icon.ion-md-quote
          .py-3.px-5.mx-5.text-white
            p.font-weight-bold.tx-24 "Mark is a sophisticated full-stack software engineer but he also understands the importance of creating good ditital customer experiences, which enables him to contribute substantively to the digital design team."
            p.pt-3 - Kevin Britton-Simmons, CEO of Scotsman Guide Media
    section#projects.bg-light.py-5
      .container
        .row
          .col-12
            .title
              h3 Projects
              span Projects I've worked on
        .row
          .col-lg-4.mb-3
            .card.h-100
              .card-body.pb-5
                h5.card-title Portfolio
                h6.card-subtitle.mb-2.text-muted aRoach
                p.card-text This is the website you're viewing now. Built with VueJs and Boostrap, it serves as a demonstration of my abilities with designing and frontend development.
                a.view(href="#") View
          .col-lg-4.mb-3
            .card.h-100
              .card-body.pb-5
                h5.card-title Project 2
                h6.card-subtitle.mb-2.text-muted aRoach
                p.card-text Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
                a.view(href="#") View
          .col-lg-4.mb-3
            .card.h-100
              .card-body.pb-5
                h5.card-title Project 1
                h6.card-subtitle.mb-2.text-muted Kincair
                p.card-text Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
                a.view(href="#") View
    section#contact.bg-white.py-5
      .container
        .row
          .col-12
            .title
              h3 Contact
              span Contact me to learn how we can work together
        .row
          .col-lg-4.mb-5.mb-lg-0
            h4.mb-3 Get in touch
            p.mb-4 Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
            .row.mb-3
              .col-6
                strong Email
              .col-6.text-nowrap mark [-at-] aroach.com
            .row.mb-3
              .col-6
                strong Phone
              .col-6.text-nowrap (713) 876-1547
            .row
              .col-6
                strong LinkedIn
              .col-6
                a(href="#") Visit
          .col-lg-6.offset-lg-2
            form
              .form-row
                .form-group.col-lg-6
                  label Name
                  input.form-control(type="text")
                .form-group.col-lg-6
                  label E-mail
                  input.form-control(type="email")
              .form-row
                .form-group.col-12
                  label Message
                  textarea.form-control(rows="5")
              .form-row
                .col-12
                  button.btn.btn-primary Send Message
</template>

<style lang="scss" scoped>
@import "../scss/theme.scss";
.home {
  .overlay {
    background-color: rgba(32, 33, 42, 0.6); // $dark in rgb
    width: 100%;
    height: 100%;

    justify-content: center;
    text-align: center;
    flex-direction: column;
    display: flex;
  }

  h3 {
    color: $white;
    text-transform: uppercase;
    font-size: 50px;

    span {
      color: $secondary;
    }
  }

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

  #home {
    width: 100%;
    height: 100vh;
    background-image: url("/images/seattle.jpg");
    background-repeat: no-repeat;
    background-size: cover;
    background-position: center;
    background-attachment: fixed;

    .photo {
      display: inline-block;
      width: 200px;
      height: 200px;
      border-radius: 50%;
      margin: 0 auto;
      border: 3px solid $primary;

      background-repeat: no-repeat;
      background-position: center -10px;
      background-size: cover;
      background-image: url("/images/me2.jpg");
    }
  }

  .quote {
    width: 100%;
    min-height: 400px;
    background-repeat: no-repeat;
    background-size: cover;
    background-position: center;
    background-attachment: fixed;

    .overlay {
      min-height: 400px;
    }

    &#quote-dev {
      background-image: url("/images/quote_bg.png");
    }

    &#quote-leader {
      background-image: url("/images/leadership.jpg");
    }
  }

  #projects {
    .card {
      position: relative;

      a.view {
        position: absolute;
        bottom: 20px;
        right: 20px;
      }
    }
  }
}
</style>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";
import Typewriter from "@/components/Typewriter.vue";

@Component({
  components: {
    Typewriter
  }
})
export default class Home extends Vue {
  toRotate: string[] = [
    "Software Engineer",
    "Web Designer",
    "Project Manager",
    "Leader",
    "Entrepreneur"
  ];

  getTypewriterText() {
    const typewriter = this.$refs.typewriter as Typewriter;
    if (typewriter) return typewriter.text;
  }

  mounted() {
    this.$forceUpdate();
  }
}
</script>
