<template>
<h1 class="card-header">{{ message }}</h1>
<p>TypeScriptとVue.jsで書きました</p>
<h2 v-on:click="doAction">クリックしてね</h2>
<h3>{{ val }} </h3>
</template>

<script lang="ts">
import { Options, Vue } from 'vue-class-component';

export default class HelloWorld extends Vue {
  message = "サンプルウェブページ"
  val = 1

  doAction():void{
    this.val += 1
  }
}
</script>
