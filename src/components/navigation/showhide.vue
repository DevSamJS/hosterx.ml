<template>
    <div class="showhide" @click="$emit('togglenavlinks')">
        +
    </div>
</template>

<script>
export default {
    name: 'showhide',
    props: {
        value:String
    },
    components: {

    }
}
</script>
<style scoped>
    .showhide {

        padding: 0px 10px;
        display: none;
        align-items: center;
        font-size: 14px;
        height: 100%;
    }
    .showhide:hover{
        background: #112757;
    }
    @media only screen and (max-width: 700px){
        .showhide {
            display: inline-grid;
            cursor: pointer;
            grid-area: showhide;
            height: 60px;
        }
    }
</style>
