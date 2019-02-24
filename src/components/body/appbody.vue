<template>
  <div class="appbody">
      <fullSizeSection title="LEARN MORE" id="learnmore"/>
      <fullSizeSection title="SIGNUP" id="signup"/>
      <fullSizeSection title="HOW TO" id="howto"/>
      <fullSizeSection title="ABOUT" id="about"/>
      <fullSizeSection title="PREMIUM" id="premium"/>
  </div>
</template>

<script>
import fullSizeSection from './fullSizeSection.vue';
export default {
  name: 'appbody',
  components: {
    fullSizeSection
  }
}
</script>

<style>
.appbody {
  color:aliceblue;
  display: grid;
  grid-auto-rows: minmax(95vh, auto);
}
.fullSizeSection {
  scroll-snap-align: start;
  padding: 20px 10px;
  background: #0c2246;
  
}
.fullSizeSection > .title {
    display: grid;
    align-items: center;
    justify-items: center;
    margin: 20px;
    height: 30px;
    opacity: 0.4;
    border-radius: 5px;
    color: #0c2246;
    background: aliceblue;
}
.content {
  padding: 10%;
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(290px, 1fr));
  grid-auto-rows: 200px;
  grid-gap: 30px 30px;
  grid-column-start: span;
}
@media only screen and (max-width: 700px){
  .fullSizeSection {
    padding: 20px 5px;
  }
  .content {
    padding: 10px 0px;
  }
}
</style>
