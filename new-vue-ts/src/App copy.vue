<template>
  <div id="app">
    <!-- <HelloWorld msg="Welcome to Your Vue.js + TypeScript App" /> -->
    {{sayHi}} {{age}} {{test}}
  </div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";
// import HelloWorld from "./components/HelloWorld.vue";

@Component({
  components: {
    //HelloWorld,
  },
})
export default class App extends Vue {

  created(): void{
    console.log(1234)
  }

  result = '';
  test = 13;
  age = 30;
  

  get sayHi(){
    return this.result = 'hello'
  }

  funcTest(something: number) {
    this.test = something;
  }
}
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
