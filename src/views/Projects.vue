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
                p.card-text This is the website you're viewing now. Built with VueJs, Boostrap and several other libraries, it serves as a demonstration of my abilities with designing and front-end development. 
                p.card-text
                  b-badge.mr-1 VueJs
                  b-badge.mr-1 Bootstrap
                  b-badge.mr-1 TypeScript
                a.view(href="https://github.com/txitguy/aroach", target="_blank") View
          .col-lg-6.col-xl-4.mb-3
            .card.h-100
              .card-body.pb-5
                h5.card-title Lending Matrix Search Engine
                h6.card-subtitle.mb-2.text-muted Scotsman Guide Media
                p.card-text I designed and built the architecture and framework level code for a lending matrix search engine, allowing brokers to search various lending scenarios for lenders that match their specific requests.
                p.card-text
                  b-badge.mr-1 .NET Core
                  b-badge.mr-1 MySQL
                  b-badge.mr-1 Couchbase
                  b-badge.mr-1 VueJs
                a.view(href="http://www.scotsmanguide.com/", target="_blank") View
          .col-lg-6.col-xl-4.mb-3
            .card.h-100
              .card-body.pb-5
                h5.card-title Realtor CRM Mobile App
                h6.card-subtitle.mb-2.text-muted Market Leader
                p.card-text I built a front-end framework using AngularJs and Ionic to develop a cross-platform hybrid mobile application.  I managed deployments on both Android and Apple app stores.
                p.card-text
                  b-badge.mr-1 AngularJs
                  b-badge.mr-1 Ionic
                  b-badge.mr-1 .NET
                a.view(href="https://apps.apple.com/us/app/market-leader-real-estate-crm/id1124558002", target="_blank") View
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
