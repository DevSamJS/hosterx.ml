<template>
      <div class="loginSignupCard" :id="button">
        <!-- <img :src="src" width="18%" :alt="title"/> -->
        <h3>{{title}}</h3>
        <input
            :style="getStyle"
            placeholder="Email"
            type="email"
            name="email"
            id="email"
        />
        <input
            placeholder="Username"
            type="username"
            name="username"
            id="username"
        />
        <input
            placeholder="Password"
            type="password"
            name="password"
            id="password"
        />
        <input
            type="button"
            :value="button"
            @click="underDevAlert()"
        />
      </div>
</template>

<script scoped>
export default {
  name: 'loginSignupCard',
  props: {
      title: String,
      button: String
  },
  components: {

  },
  computed: {
      getStyle: function(){
          if(this.button=='Login')
          return {
            visibility: 'hidden'
          }
          else return {}
      }
  },
  methods: {
      underDevAlert: function(){
          alert('Under Development!')
      }
  }
}
</script>

<style scoped>
.loginSignupCard {
  display: grid;
  justify-items: center;
  align-items: center;
  background: aliceblue;
  color: #0c2246;
  border-radius: 8px;
  box-shadow: 10px 10px 10px black;
  padding: 50px 0px 50px 0px;
}
.loginSignupCard > h3{
  margin: 20px 20px;
  text-align: center;
}
.loginSignupCard > input {
    /* color: aliceblue; */
    background: aliceblue;
    font-weight: 700;
    padding-left: 15px;
    border: 0px;
    border-bottom: 1px solid #0c2246;
    /* border-radius: 0px 0px 0px 10px; */
    width: 250px;
    height: 50px;
}
.loginSignupCard > input[type="button"] {
    background: orange;
    width: 265px;
    border-radius: 5px;
    border: 0px;
}
</style>
