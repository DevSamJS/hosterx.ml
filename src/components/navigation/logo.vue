<template>
    <div class="logo">
        <h2><a href="#">@HOSTERXML</a></h2>
    </div>
</template>

<script>
export default {
    name: 'logo',
    components: {

    }
}
</script>
<style scoped>
    .logo {
        cursor: pointer;
        max-height: 60px;
        display: flex;
        align-items: center;
        grid-area: logo;
        padding: 0px 10px;
    }
    .logo:hover {
        background-color: #112757;
    }
    .logo > h2 > a {
        color: aliceblue;
        text-decoration: none;
    }
</style>
