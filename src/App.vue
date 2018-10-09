<template>
    <Container></Container>
</template>

<script>
    import Container from "@/components/Container";

    export default {
        name: 'app',
        components: {
            Container
        }
    }
</script>

<style>
    body {
        margin: 0 auto;
    }

    #app {
        font-family: 'Avenir', Helvetica, Arial, sans-serif;
        -webkit-font-smoothing: antialiased;
        -moz-osx-font-smoothing: grayscale;
        background: #222;
        margin: 0;
        padding: 0;
    }
</style>
