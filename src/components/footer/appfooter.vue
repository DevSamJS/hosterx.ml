<template>
  <div class="appfooter">
    <b>Copyright @2019 - Hosterx.ml</b>
  </div>
</template>

<script>
export default {
  name: 'appfooter',
  components: {

  }
}
</script>

<style>
.appfooter {
    background: #0c2246;
    color: aliceblue;
    display: grid;
    grid-template-columns: repeat(10, 1fr);
    grid-template-rows: repeat(3, 1fr);
    grid-template-areas: 
        ". . . . . . . . . ."
        ". . . copyright copyright copyright copyright . . ."
        ". . . . . . . . . .";
}
.appfooter > b {
    display: inline-grid;
    grid-area: copyright;
    align-items: center;
    justify-items: center;
}
</style>
