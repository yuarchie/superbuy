<template>
    <div class="header-middle">
        <el-row type="flex" align="middle" justify="space-between">
            <el-col :span="6">
                <a href="localhost:8080" class="header-logo" title="Superbuy首页"></a>
            </el-col>
            <el-col :span="12">
                <el-tabs style="margin-bottom: 10px" type="card" value="first">
                    <el-tab-pane label="代购享返利" name="first">
                        <el-input placeholder="粘贴你要代购商品的链接或输入名称" class="input-with-select">
                            <el-button slot="append" icon="el-icon-goods">去购买</el-button>
                        </el-input>
                    </el-tab-pane>
                    <el-tab-pane label="社区" name="second">
                        <el-input placeholder="输入社区帖子关键字" class="input-with-select">
                            <el-button slot="append" icon="el-icon-search">搜索</el-button>
                        </el-input>
                    </el-tab-pane>
                </el-tabs>
                <span>中国电商商品轻松淘，</span>
                <a href="https://www.taobao.com/" target="_black" style="color: #ff5305;">淘宝</a>
                <span>、</span>
                <a href="https://www.tmall.com/" target="_black" style="color: #ff5305;">天猫</a>
                <span>、</span>
                <a href="https://www.jd.com/" target="_black" style="color: #ff5305;">京东</a>
                <span>等平台商品均有返利</span>
            </el-col>
            <el-col :span="3">
                <dl class="header-service header-icon">
                    <dt><span style="color: #999">存在疑问？</span></dt>
                    <dt><span>咨询</span><a href="https://www.taobao.com/" target="_black">在线客服</a></dt>
                </dl>
            </el-col>
            <el-col :span="3">
                <dl class="header-expert header-icon">
                    <dt><span style="color: #999">找不到商品？</span></dt>
                    <dt><span>试试</span><a href="https://www.taobao.com/" target="_black">专家购</a></dt>
                </dl>
            </el-col>
        </el-row>
    </div>
</template>

<script>
    export default {
        name: "HeaderMiddle"
    }
</script>

<style scoped>

    .header-icon{
        float: right;
        min-height: 50px;
        padding-left: 50px;
    }

    .header-service {
        background: url(../assets/icon/header_icon_b_service.png) no-repeat;
    }

    .header-expert {
        background: url(../assets/icon/header_icon_b_expert.png) no-repeat;
    }
    a{
        color:#1268bb ;
    }

    a:link, a:visited {
        text-decoration: none;
    }

    a:hover {
        text-decoration: underline;
    }

    .header-middle {
        font-size: 12px;
        color: #666666;
        width: 1190px;
        margin: 0 auto;
    }

    .header-logo {
        display: block;
        float: left;
        width: 158px;
        height: 160px;
        background: url("../assets/icon/header_logo_cn.png") center no-repeat;
    }

</style>
