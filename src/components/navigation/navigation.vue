<template>
    <div class="navigation">
        <logo/>
        <showhide @togglenavlinks="toggleNavlinks()"/>
        <navlinks/>
    </div>
</template>

<script>
import logo from './logo';
import showhide from './showhide';
import navlinks from './navlinks';

export default {
    name: 'navigation',
    data(){
        return {
            
        }
    },
    components: {
        logo,
        showhide,
        navlinks
    },
    methods: {
        toggleNavlinks: function(){
            const el = document.getElementsByClassName('navlinks')[0];
            if(el.style.display=='' || el.style.display=='none'){
                el.style.display='grid';
            }
            else{
                el.style.display='none';
            }
        }
    },
    computed: {
        
    }
}
</script>

<style scoped>
    .navigation {
        scroll-snap-align: start;
        min-height: 60px;
        display: grid;
        grid-template-columns: max-content auto max-content;
        grid-template-rows: 60px;
        grid-template-areas:
                "logo . navlinks";
        background-color: #0c2246;
        color: aliceblue;
    }
    @media only screen and (max-width: 700px){
        .navigation {
            grid-template-rows: repeat(max-contant,60px);
            grid-template-areas:
                "logo . showhide"
                "navlinks navlinks navlinks"
                "navlinks navlinks navlinks"
                "navlinks navlinks navlinks"
                "navlinks navlinks navlinks";
            background-color: #0c2246;
            color: aliceblue;
        }
    }
</style>