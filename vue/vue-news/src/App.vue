<template>
  <div id="app">

    <!--등록할때는 벡터로 쓰고 등록할때는 dash 로 등록한다.-->
    <tool-bar></tool-bar>
    <transition name="page">
    <!-- url이 만약 news  -->
    <!-- <NewsView></NewsView> -->
    <router-view></router-view> <!-- url 지정해 줬던, index.js 위치에 path, component 불러온다. -->
    </transition>
  </div>
</template>

<script>
  /*eslint-disable*/
  import ToolBar from './components/ToolBar.vue';

export default {
  components : {
    ToolBar,
  },
}
</script>
  
<style>
/* 라우터 트랜지션 */
.page-enter-active, .page-leave-active {
  transition: opacity .5s;
}
.page-enter, .page-leave-to /* .fade-leave-active below version 2.1.8 */ {
  opacity: 0;
}
</style>
