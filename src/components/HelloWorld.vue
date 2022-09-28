<template>
  <h1>今日の運勢</h1>
  <p v-on:click="doAction">クリックして占う</p>
  <p> {{ val }}</p>

</template>

<script lang="ts">
import { Options, Vue } from 'vue-class-component';

export default class HelloWorld extends Vue {
 val = ""
  doAction(): void {
    const unsei = ["🌸🌸🌸大吉🌸🌸🌸", "😇😇😇大凶😇😇😇", "👿👿👿凶👿👿👿"]
    this.val = unsei[this.getRandomInt(unsei.length)]
  }
  
  getRandomInt(max: number) {
    return Math.floor(Math.random() * max);
  }
}
</script>
