<template lang="pug">
  #app
    .container-fluid
      #navbar-wrapper.row.min-vh-100
        aside.p-0.bg-dark
          b-navbar.flex-row.flex-lg-column(toggleable="lg", type="dark")
            b-navbar-brand.logo(href="#")
              a(href="/")
                img(src="./assets/logo.png", alt="aRoach Website")
            b-navbar-toggle(target="nav-collapse")
            b-collapse#nav-collapse.w-100(is-nav)
              b-navbar-nav.flex-lg-column
                b-nav-item.active(href="#home")
                  i.icon.ion-md-home
                  | Home
                b-nav-item(href="#about")
                  i.icon.ion-md-person
                  | About me
                b-nav-item(href="#experience")
                  i.icon.ion-md-list
                  | Experience
                b-nav-item(href="#projects")
                  i.icon.ion-md-code
                  | Projects
                b-nav-item(href="#contact")
                  i.icon.ion-md-chatboxes
                  | Contact
                b-nav-item.d-lg-none(href="https://www.linkedin.com/in/roachm/")
                  i.icon.ion-logo-linkedin
                  | LinkedIn
          .d-none.d-lg-block.text-center.tx-18.mb-5
            a(href="https://www.linkedin.com/in/roachm/", target="_blank")
              i.icon.ion-logo-linkedin.mr-2.text-primary
              span.text-white LinkedIn

        main.col.bg-faded.p-0.offset-lg-2
          router-view

        .col-12.text-right.mb-3.tx-12 Copyright &copy; 2019, aRoach.com
</template>

<style lang="scss" scoped>
@import "scss/theme.scss";

#app {
  #navbar-wrapper {
    aside {
      position: fixed;
      z-index: 100;
    }
    .nav-item.active > a {
      color: $primary;
    }
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

      aside {
        width: 100%;
      }
    }
  }

  @include media-breakpoint-up(lg) {
    #navbar-wrapper {
      aside {
        width: 250px;
        display: flex;
        justify-content: space-between;
        flex-direction: column;

        height: 100vh;
      }
      .logo {
        height: 150px;
        width: 100%;
        justify-content: center;
        text-align: center;
        flex-direction: column;
        display: flex;
      }
      main {
        margin-left: 250px !important;
      }
    }
  }
}
</style>

<script lang="ts">
import { Vue, Component } from "vue-property-decorator";

@Component
export default class extends Vue {
  mounted() {
    document.querySelectorAll('a[href^="#"]').forEach(anchor => {
      anchor.addEventListener("click", function(this: HTMLElement, e: Event) {
        e.preventDefault();

        document.querySelector(this.getAttribute("href")!)!.scrollIntoView({
          behavior: "smooth"
        });
      });
    });
  }
}
</script>
