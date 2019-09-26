<template lang="pug">
  .typing
    p {{base}}{{text}}
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";

@Component({
  props: {
    toRotate: Array,
    period: {
      type: Number,
      default: 2000
    },
    base: String
  }
})
export default class Typewriter extends Vue {
  period: number = 2000;
  loopNum: number = 0;
  isDeleting: boolean = false;
  text: string = "";

  mounted() {
    this.typingTick();
  }

  typingTick() {
    let i = this.loopNum % this.$props.toRotate.length;
    let fullTxt = this.$props.toRotate[i];

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

    setTimeout(this.typingTick, delta);
  }
}
</script>
