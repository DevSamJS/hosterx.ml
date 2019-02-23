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
        font-size: 15px;
        font-weight: 600;
        display: inline-grid;
        align-items: center;
        background: #0c2246;
        color: aliceblue;
        text-align: center;
        text-decoration: none;
    }
    .btn:hover {
      background: #0c2246;
      opacity: 0.94;
    }
    @media only screen and (max-width: 700px){
      /* .btn{
        font-size: 12px;
      } */
    }
</style>
