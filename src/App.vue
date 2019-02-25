<template>
  <div id="app">
    <navigation/>
    <appheader />
    <appbody />
    <appfooter/>
  </div>
</template>

<script>
import navigation from './components/navigation/navigation.vue';
import appheader from './components/header/apphead.vue';
import appbody from './components/body/appbody.vue';
import appfooter from './components/footer/appfooter.vue';
export default {
  name: 'app',
  components: {
    navigation,
    appheader,
    appbody,
    appfooter
  }
}
</script>

<style>
*{
  margin: 0px;
  font-family: monospace;
}
body {
  display: grid;
  grid-template-columns: auto minmax(300px,1500px) auto;
  grid-template-rows: auto;
  grid-template-areas:
      ". app .";
  scroll-snap-type:y proximity;
  overflow-y: scroll;
  background: #0c2246;
}

#app {
  grid-area: app;
  display: grid;
  grid-template-columns: auto;
  grid-template-rows: auto minmax(400px, auto) minmax(768px, auto) 100px;
}


</style>
