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
                {value:'#freehosting', href: '#freehosting'},
                {value:'#premium', href: '#premium'},
                {value:'#howto', href: '#howto'},
                {value:'#aboutus', href: '#about'},
                {value:'#clientarea', href: '#clientarea'},
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
