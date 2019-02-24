<template>
      <div class="featureCard">
        <img :src="src" width="18%" :alt="title"/>
        <h3>{{title}}</h3>
        <p style="
            margin: -20px 20px 10px 20px;
            text-align: center;
        ">{{discription}}</p>
      </div>
</template>

<script scoped>
export default {
  name: 'featureCard',
  props: {
      title: String,
      discription: String,
      src: String
  },
  components: {

  }
}
</script>

<style scoped>
.featureCard {
  display: grid;
  justify-items: center;
  align-items: center;
  background: aliceblue;
  color: #0c2246;
  border-radius: 8px;
  box-shadow: 10px 10px 10px black;
}
</style>
