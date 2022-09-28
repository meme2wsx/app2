<template>
  <h1>今日の運勢</h1>
  <p>ブラウザのリロードで運勢が表示されます</p>
  <p class="alert alert-info"> {{ unsei }}</p>
  <p>算出プロパティを使いました</p>
</template>

<script lang="ts">
import { Options, Vue } from 'vue-class-component';

export default class HelloWorld extends Vue {

  get unsei(): string {
    const unArray = ["🌸大吉🌸", "😇大凶😇", "👿凶👿"]
    return unArray[Math.floor(Math.random() * unArray.length)]
  }
}
</script>
