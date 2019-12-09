<template>
  <div class="container mx-auto px-4 py-4" id="app">
    <Header />
    <Contents msg="This is props sending test" v-bind:weather="weather"/>
    <!-- 현재 props에서 자식 컴포넌트에 props를 보내기 위해 v-bind를 사용 -->
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import Header from './components/Header.vue';
import Contents from './components/Contents.vue';
// react.js 처럼 컴포넌트들을 받아온다
let searchLocation;
let weatherData;
 fetch(`https://search.naver.com/search.naver?sm=top_hty&fbm=1&ie=utf8&query=${searchLocation}`)
    .then(res => res.json())
    .then(data =>  weatherData = data)
// props에 정의될 데이터를 미리 받아오는 활동은 스크립트 안에서 실행한다.

@Component({
  // 이 컴포넌트에서 렌더링할 컴포넌트들을 components:{} 안에 집어 넣는다 그럼 templates 태그 안에서 사용가능하다.
  components: {
    Header,
    Contents,
  },
  // props의 정의를 할때 부모로 부터 받아와서 사용할 props는 props:{}를 통해 정의하고 직접 만들어 props로 쓸 것들은 data 함수로 받아온다
  data: () => {
    return {
      weather: 'test hellos'
    }
  }
})
export default class App extends Vue {
  
}
</script>

<style>

</style>
