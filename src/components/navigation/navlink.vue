<template>
    <a class="navlink" :href="href">
        {{value}}
    </a>
</template>

<script>
export default {
    name: 'navlink',
    props: {
        value:String,
        href:String
    },
    components: {

    }
}
</script>
<style scoped>
    .navlink {
        padding: 0px 10px;
        display: inline-grid;
        justify-items: center;
        align-items: center;
        font-size: 14px;
        height: 100%;
        color: aliceblue;
        text-decoration: none;
    }
    .navlink:hover{
        background: #112757;
    }
    @media only screen and (max-width: 700px){
        .navlink {
            padding: 0px;
            font-size: 16px;
            color: #0c2246;
            height: 60px;
            width: 100%;
        }
        .navlink:hover{
            color: aliceblue;
        }
    }
</style>
