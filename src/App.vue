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
                b-nav-item.active(href="#")
                  i.icon.ion-md-home
                  | Home
                b-nav-item(href="#")
                  i.icon.ion-md-person
                  | About me
                b-nav-item(href="#")
                  i.icon.ion-md-list
                  | Experience
                b-nav-item(href="#")
                  i.icon.ion-md-code
                  | Projects
                b-nav-item(href="#")
                  i.icon.ion-md-document
                  | Blog
                b-nav-item(href="#")
                  i.icon.ion-md-chatboxes
                  | Contact

        main.col.bg-faded.p-0
          router-view
</template>

<style lang="scss" scoped>
@import "scss/theme.scss";

#app {
  #navbar-wrapper {
    .nav-link {
      font-size: 20px;
      i.icon {
        display: inline-block;
        width: 24px;
      }
    }
  }

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
