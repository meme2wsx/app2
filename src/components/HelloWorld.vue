<template>
<h1 class="card-header">{{ message }}</h1>
<p>TypeScriptとVue.jsで書きました</p>
</template>

<script lang="ts">
import { Options, Vue } from 'vue-class-component';

export default class HelloWorld extends Vue {
  message = "サンプルウェブページ"
}
</script>
