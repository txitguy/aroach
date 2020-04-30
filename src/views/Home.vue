<template lang="pug">
  .home
    section#home
      .overlay
        .photo
        h3.mt-3
          | Mark
          span  Roach
        Typewriter.text-white.tx-24(:toRotate="toRotate", base="I'm a ", ref="typewriter")
    About
    section#quote-leader.quote
      .overlay
        .container
          h3
            span
              i.icon.ion-md-quote
          .py-3.px-5.mx-5.text-white
            p.font-weight-bold.tx-24 "Mark is a strong, organized manager who has high standards but also consistently demonstrates compassion for his co-workers."
            p.pt-3 - Kevin Britton-Simmons, CEO of Scotsman Guide Media
    Experience
    section#quote-dev.quote
      .overlay
        .container
          h3
            span
              i.icon.ion-md-quote
          .py-3.px-5.mx-5.text-white
            p.font-weight-bold.tx-24 "Mark is a sophisticated full-stack software engineer but he also understands the importance of creating good ditital customer experiences, which enables him to contribute substantively to the digital design team."
            p.pt-3 - Kevin Britton-Simmons, CEO of Scotsman Guide Media
    Projects
    Contact
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

  #home {
    width: 100%;
    height: 100vh;
    background-image: url("/images/seattle.jpg");
    background-repeat: no-repeat;
    background-size: cover;
    background-position: center;
    background-attachment: fixed;

    @include media-breakpoint-down(md) {
      background-attachment: scroll;
    }

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

    @include media-breakpoint-down(md) {
      background-attachment: scroll;
    }

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
}
</style>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";
import Typewriter from "@/components/Typewriter.vue";
import About from "@/views/About.vue";
import Experience from "@/views/Experience.vue";
import Projects from "@/views/Projects.vue";
import Contact from "@/views/Contact.vue";

@Component({
  components: {
    Typewriter,
    About,
    Experience,
    Projects,
    Contact
  }
})
export default class Home extends Vue {
  toRotate: string[] = [
    "Software Engineer",
    "Web Designer",
    "Project Manager",
    "Digital Marketer",
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
