<template lang="pug">
  .projects
    section#projects.bg-light.py-5
      .container
        .row
          .col-12
            .title
              h3 Projects
              span Projects I've worked on
        .row
          .col-lg-6.col-xl-4.mb-3
            .card.h-100
              .card-body.pb-5
                h5.card-title Portfolio
                h6.card-subtitle.mb-2.text-muted aRoach
                p.card-text This is the website you're viewing now. Built with VueJs and Boostrap, it serves as a demonstration of my abilities with designing and frontend development.
                a.view(href="#") View
          .col-lg-6.col-xl-4.mb-3
            .card.h-100
              .card-body.pb-5
                h5.card-title Project 2
                h6.card-subtitle.mb-2.text-muted aRoach
                p.card-text Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
                a.view(href="#") View
          .col-lg-6.col-xl-4.mb-3
            .card.h-100
              .card-body.pb-5
                h5.card-title Project 1
                h6.card-subtitle.mb-2.text-muted Kincair
                p.card-text Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
                a.view(href="#") View
</template>

<style lang="scss" scoped>
@import "../scss/theme.scss";
.projects {
  .card {
    position: relative;

    a.view {
      position: absolute;
      bottom: 20px;
      right: 20px;
    }
  }
}
</style>
