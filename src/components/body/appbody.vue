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

<style scoped>
.appbody {
  color:aliceblue;
  display: grid;
  grid-template-rows: repeat(2,minmax(700px, max-content));
}
</style>
