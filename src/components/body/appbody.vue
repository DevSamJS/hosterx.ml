<template>
  <div class="appbody">
      <div id="learnmore">
        Learn More
      </div>
      <div id="signup">
        SignUp
      </div>
  </div>
</template>

<script>
export default {
  name: 'appbody',
  components: {
  }
}
</script>

<style scoped>
.appbody {
  color:aliceblue;
  display: grid;
  grid-template-rows: repeat(2,minmax(700px, max-content));
  grid-gap: 0.5px;
  scroll-snap-type: y mandatory; 
}
#learnmore {
  padding: 10px;
  background: #0c2246;
}
#signup {
  padding: 10px;
  background: #0c2246;
}
</style>
