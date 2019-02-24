<template>
    <div class="navlinks">
        <navlink
            name="navlinksElement"
            :key="navlink.value"
            v-for="navlink in navlinks"
            :value="navlink.value"
            :href="navlink.href"/>
    </div>
</template>

<script>
import navlink from './navlink'
export default {
    name: 'navlinks',
    data: function(){
        return {
            navlinks: [
                {value:'Freehosting', href: '#learnmore'},
                {value:'Premium', href: '#premium'},
                {value:'Howto', href: '#howto'},
                {value:'Aboutus', href: '#about'},
                {value:'Clientarea', href: '#Login'},
            ]
        }
    },
    components: {
        navlink
    },
    methods: {
        
    }
}
</script>
<style scoped>
    .navlinks {
        cursor: pointer;
        display: grid;
        justify-items: center;
        align-items:center;
        grid-template-columns: repeat(5, auto);
        grid-template-rows: 60px;
        grid-area: navlinks;
    }
    @media only screen and (max-width: 700px){
        .navlinks {
            display: none;
            grid-template-columns: auto;
            background: orange;
        }
    }
</style>
