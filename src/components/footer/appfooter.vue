<template>
  <div class="appfooter">
    <b>Copyright @ {{(new Date()).getFullYear()}} - {{getHostname}}</b>
    <h4 style="display:inline-grid;">Created by: Sameer Tariq (@imsamtar)</h4>
  </div>
</template>

<script>
export default {
  name: 'appfooter',
  computed: {
      getHostname: function(){
          return window.location.hostname;
      }
  },
  components: {

  }
}
</script>

<style>
.appfooter {
    scroll-snap-align: end;
    border-top: 3px dotted aliceblue;
    background: #0c2246;
    color: aliceblue;
    display: grid;
    grid-template-columns: repeat(10, 1fr);
    grid-template-rows: 40px repeat(2, 25px);
    grid-template-areas:
        ". . . . . . . . . ."
        "copyright copyright copyright copyright copyright copyright copyright copyright copyright copyright"
        "createdby createdby createdby createdby createdby createdby createdby createdby createdby createdby ";
}
.appfooter > b {
    display: inline-grid;
    grid-area: copyright;
    align-items: center;
    justify-items: center;
}
.appfooter > h4 {
    display: inline-grid;
    grid-area: createdby;
    align-items: center;
    justify-items: center;
}
/* @media only screen and (max-width: 700px){
    
} */
</style>
