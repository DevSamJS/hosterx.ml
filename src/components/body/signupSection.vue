<template>
  <div class="signupSection fullSizeSection" :id="id">
    <h3>{{title}}:-
      <a href="#">X</a>
      <a href="#learnmore">UP</a>
      <a href="#howto">DOWN</a>
    </h3>
    <hr>
    <div class="content">
      <loginSignupCard
        :key="loginSignupCard.button"
        v-for="loginSignupCard in loginSignupCards"
        :button="loginSignupCard.button"
        :title="loginSignupCard.title"
      />
    </div>
  </div>
</template>

<script>
import loginSignupCard from './cards/loginSignupCard'
export default {
  name: 'signupSection',
  props: {
      title: String,
      id: String
  },
  data: function(){
    return {
      loginSignupCards: [
        {
          title: "Already have account login here ...",
          button: "Login"
        },
        {
          title: `Create one for free right now ...`,
          button: "Signup"
        }
      ]
    }
  },
  components: {
    loginSignupCard
  }
}
</script>

<style scoped>
.content {
  grid-template-columns: repeat(2, minmax(290px, 1fr));
  grid-auto-rows: 500px;
}
@media only screen and (max-width: 700px){
  .content {
    grid-template-columns: repeat(1, minmax(290px, 1fr));
    grid-auto-rows: 500px;
  }
}
</style>
