<template>
  <div class="container mx-auto px-4 py-4" id="app">
    <Header />
    <Contents msg="This is props sending test" />
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import Header from './components/Header.vue';
import Contents from './components/Contents.vue';

@Component({
  components: {
    Header,
    Contents,
  },
})
export default class App extends Vue {}
</script>

<style>

</style>
