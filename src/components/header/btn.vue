<template>
  <a :style="styl" class="btn" :href="href" >
    {{value}}
  </a>
</template>

<script>
export default {
  name: 'btn',
  props: {
    classes: String,
    value: String,
    href: String,
    styl: String
  },
  components: {

  }
}
</script>

<style scoped>
    .btn {
        font-size: 13px;
        font-weight: 700;
        display: inline-grid;
        align-items: center;
        background: black;
        color: aliceblue;
        text-align: center;
        text-decoration: none;
    }
    .btn:hover {
      background: black;
      opacity: 0.9;
    }
    @media only screen and (max-width: 700px){
      /* .btn{
        font-size: 12px;
      } */
    }
</style>
