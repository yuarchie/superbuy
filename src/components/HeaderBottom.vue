<template>

    <el-row style="background: #142341" type="flex" align="middle" justify="center">
        <el-col style="width: 1190px" :span="24">
            <el-menu
                    :default-active="activeIndex2"
                    class="el-menu-demo"
                    mode="horizontal"
                    @select="handleSelect"
                    background-color="#142341"
                    text-color="#fff"
                    active-text-color="#fff">
                <el-menu-item id="index" index="1">首页</el-menu-item>
                <el-menu-item index="2">代购</el-menu-item>
                <el-menu-item index="3">优选商场</el-menu-item>
                <el-menu-item index="4">转运</el-menu-item>
                <el-menu-item index="5">虚拟代充</el-menu-item>
                <el-menu-item index="5">社区</el-menu-item>
                <el-menu-item index="5">机票</el-menu-item>
                <el-menu-item index="5">商务合作</el-menu-item>
                <el-menu-item index="5">专家合作</el-menu-item>
                <el-menu-item index="5">推广联盟</el-menu-item>
            </el-menu>
        </el-col>
    </el-row>
</template>

<script>
    export default {
        name: "HeaderBottom"
    }
</script>

<style scoped>

    .el-menu-demo {
        border-bottom: none !important;
    }

    .el-menu-demo .el-menu-item {
        height: 36px;
        line-height: 36px;
        border-bottom: none;
    }

    .el-menu-demo .el-menu-item:hover {
        background: #0d3770 !important;
    }

    #index {
        background: #1268bb !important;
    }

    .el-menu-demo  .el-menu-item.is-active {
        border-bottom: none;
    }


</style>
