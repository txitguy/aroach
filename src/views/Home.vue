<template lang="pug">
  .home
    section#seattle
      .overlay
        .photo
        h3.mt-3
          | Mark
          span  Roach
        .typing
          p.tx-24 I'm a
            span(ref='typing')
              span.wrap {{text}}
</template>

<style lang="scss" scoped>
@import "../scss/theme.scss";
.home {
  #seattle {
    width: 100%;
    height: 100vh;
    background-image: url("/images/seattle.jpg");
    background-repeat: no-repeat;
    background-size: cover;
    background-position: center;

    .overlay {
      background-color: rgba(0, 0, 0, 0.5);
      width: 100%;
      height: 100%;

      justify-content: center;
      text-align: center;
      flex-direction: column;
      display: flex;
    }

    .photo {
      display: inline-block;
      width: 200px;
      height: 200px;
      border-radius: 50%;
      margin: 0 auto;
      border: 3px solid $info;

      background-repeat: no-repeat;
      background-position: center center;
      background-size: cover;
      background-image: url("/images/me.jpg");
    }

    h3 {
      color: $white;
      text-transform: uppercase;
      font-size: 50px;

      span {
        color: $warning;
      }
    }

    .typing {
      color: $white;
    }
  }
}
</style>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";

@Component
export default class Home extends Vue {
  toRotate: string[] = [
    " Software Engineer",
    " Web Designer",
    " Leader",
    "n Entrepreneur"
  ];
  period: number = 2000;
  loopNum: number = 0;
  isDeleting: boolean = false;
  text: string = "";

  mounted() {
    this.TypingTick();
  }

  TypingTick() {
    let i = this.loopNum % this.toRotate.length;
    let fullTxt = this.toRotate[i];

    if (this.isDeleting) {
      this.text = fullTxt.substring(0, this.text.length - 1);
    } else {
      this.text = fullTxt.substring(0, this.text.length + 1);
    }

    let delta = 200 - Math.random() * 100;
    if (this.isDeleting) delta /= 2;

    if (!this.isDeleting && this.text === fullTxt) {
      delta = this.period;
      this.isDeleting = true;
    } else if (this.isDeleting && this.text === "") {
      this.isDeleting = false;
      this.loopNum++;
      delta = 500;
    }

    setTimeout(this.TypingTick, delta);
  }
}
</script>
