<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <HelloWorld msg="Appコンポーネントからこの文字列を渡しています" />
</template>

<script lang="ts">
import { Options, Vue } from 'vue-class-component';
import HelloWorld from './components/HelloWorld.vue';

// @から始まるものは、デコレーターといい、@Options以外にも色々ある
// 下のAppクラスに付与するオプション
// AppクラスがHelloWorldコンポーネントを使えるようにするためにやっているのだ
//ためしに @Options()の定義を消すとどうなるか見てみると理解が早いはず
@Options({
  components: {
    HelloWorld,
  },
})
export default class App extends Vue {}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
