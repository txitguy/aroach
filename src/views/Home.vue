<template lang="pug">
  .home
    h1 WTF HOMIE
    img(alt="Vue logo", src="../assets/logo.png") 
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";

@Component
export default class Home extends Vue {}
</script>
