<template>
  <div class="appbody">
      <learnmoreSection title="LEARN MORE" id="learnmore"/>
      <signupSection title="SIGNUP" id="signup"/>
      <howtoSection title="HOW TO" id="howto"/>
      <aboutSection title="ABOUT" id="about"/>
      <premiumSection title="PREMIUM" id="premium"/>
  </div>
</template>

<script>
import learnmoreSection from './learnmoreSection';
import signupSection from './signupSection';
import howtoSection from './howtoSection';
import aboutSection from './aboutSection';
import premiumSection from './premiumSection';
export default {
  name: 'appbody',
  components: {
    learnmoreSection,
    signupSection,
    howtoSection,
    aboutSection,
    premiumSection
  }
}
</script>

<style>
.appbody {
  color: aliceblue;
  display: grid;
  grid-auto-rows: minmax(700px, auto);
}
.fullSizeSection {
  scroll-snap-align: start;
  padding: 20px 10px;
  /* background: #0c2246; */
  
}
.fullSizeSection > h3 > a {
  float: right;
  color: aliceblue;
  text-decoration: none;
  margin: 0px 5px;
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
  padding: 50px 10%;
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(290px, 1fr));
  grid-auto-rows: minmax(200px, auto);
  grid-gap: 30px 30px;
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
