<template>
  <div class="fullSizeSection" :id="id">
    <h3>{{title}}:-<a href="#" style="float: right;color: aliceblue; text-decoration: none">X</a></h3>
    <hr>
  </div>
</template>

<script scoped>
export default {
  name: 'fullSizeSection',
  props: {
      title: String,
      id: String
  },
  components: {

  }
}
</script>

<style scoped>
.fullSizeSection {
  scroll-snap-align: start;
  height: 768px;
  padding: 10px;
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
</style>
