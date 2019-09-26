<template lang="pug">
  #app
    .container-fluid
      #navbar-wrapper.row.min-vh-100
        aside.col-lg-2.p-0.bg-dark
          //.logo.text-center.justify-content-center.flex-column.text-light.border-bottom.d-none.d-lg-flex aRoach
          b-navbar.flex-row.flex-lg-column(toggleable="lg", type="dark")
            b-navbar-brand.logo(href="#") aRoach
            b-navbar-toggle(target="nav-collapse")
            b-collapse#nav-collapse.w-100(is-nav)
              b-navbar-nav.flex-lg-column
                b-nav-item(href="#")
                  font-awesome-icon(icon="home")
                  | Home
                b-nav-item(href="#" disabled) Disabled

        main.col.bg-faded.py-3
          router-view


  
    //- .container-fluid
    //-   #navbar-wrapper.row.min-vh-100
    //-     aside.col-lg-2.p-0.bg-dark
    //-       nav.navbar.navbar-expand-lg.navbar-dark.bg-dark.flex-lg-column.flex-row.align-items-start.py-2
    //-         button.navbar-toggler(type="button", data-toggle="collapse", data-target="#navbar", aria-controls="navbar", aria-expanded="false", aria-label="Toggle navigation")
    //-           span.navbar-toggler-icon
    //-         #navbar.collapse.navbar-collapse
    //-           ul.flex-lg-column.flex-row.navbar-nav.w-100.justify-content-between
    //-             li.nav-item
    //-               a.nav-link.pl-0.text-nowrap(href="#")
    //-                 font-awesome-icon(icon="user-secret")
    //-                 span.font-weight-bold  Home
    //-             li.nav-item
    //-               a.nav-link.pl-0.text-nowrap(href="#")
    //-                 font-awesome-icon(icon="user-secret")
    //-                 span.font-weight-bold  Link
    //-             li.nav-item
    //-               a.nav-link.pl-0.text-nowrap(href="#")
    //-                 font-awesome-icon(icon="user-secret")
    //-                 span.font-weight-bold  Link
    //-             li.nav-item
    //-               a.nav-link.pl-0.text-nowrap(href="#")
    //-                 font-awesome-icon(icon="user-secret")
    //-                 span.font-weight-bold  Link
    //-     main.col.bg-faded.py-3
    //-       router-view
</template>

<style lang="scss" scoped>
@import "scss/theme.scss";

#app {
  @include media-breakpoint-down(md) {
    #navbar-wrapper {
      min-height: initial !important;
    }
  }

  @include media-breakpoint-up(lg) {
    aside {
      min-width: 250px;
    }
    #navbar-wrapper {
      .logo {
        height: 150px;
        width: 100%;
        justify-content: center;
        text-align: center;
        flex-direction: column;
        display: flex;
      }
    }
  }
}
</style>

<script lang="ts">
import { Vue, Component } from "vue-property-decorator";

@Component
export default class extends Vue {
  mounted() {}
}
</script>
