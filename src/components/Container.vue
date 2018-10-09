<template>
    <el-container direction="vertical">
        <AlertWarning/>
        <el-header height="227px">
            <header-top-main/>
            <header-middle/>
            <header-bottom/>
        </el-header>
        <el-main style=" background-color: #f5f5f5;margin: 0">
            <HomePage/>
        </el-main>
        <el-footer></el-footer>
    </el-container>
</template>

<script>
    import HeaderTopMain from "@/components/HeaderTop";
    import AlertWarning from "@/components/AlertWarning";
    import HeaderMiddle from "@/components/HeaderMiddle";
    import HeaderBottom from "@/components/HeaderBottom";
    import HomePage from "@/components/HomePage";

    export default {
        name: "container",
        components: {HomePage, HeaderBottom, HeaderMiddle, AlertWarning, HeaderTopMain}
    }
</script>

<style scoped>
    .el-header,.el-main{
        margin: 0;
        padding: 0;
    }

    .el-main {

    }

    .el-footer {

    }
</style>
