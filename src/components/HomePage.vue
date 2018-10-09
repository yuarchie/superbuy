<template>
    <div class="home-page">
        <div class="banner">
            <el-carousel height="360px">
                <el-carousel-item :label="bannerLabels[item-1]" v-for="item in 4" :key="item">
                    <a :href="bannerHrefs[item-1]"><img :src="banners[item-1]"/></a>
                </el-carousel-item>
            </el-carousel>
        </div>
        <div class="user-info">
            <el-card style="height: 360px" :body-style="{ padding: '0px',background: '#6da2ed',height:'100%' }"
                     class="box-card" shadow="hover">
                <div slot="header" class="user-header">

                    <a href="https://www.taobao.com">
                        <img src="../assets/icon/user_performance.png"/>
                    </a>

                    <dl>
                        <dt style="margin-bottom: 10px">
                            <span>欢迎来到Superbuy</span>
                        </dt>
                        <dt>
                            <el-button size="mini" plain>登陆</el-button>
                            <el-button size="mini" plain>注册</el-button>
                        </dt>
                    </dl>
                </div>
                <div class="user-body-header">
                    <a href="https://www.taobao.com/">
                        <span>为什么选择Superbuy?</span>
                    </a>
                </div>
                <div class="user-body-item" v-for="item in 3" :key="item">
                    <div><span>{{userLabels[item-1][0]}}</span></div>
                    <div><a :href="userHrefs[item-1]"> <span>{{userLabels[item-1][1]}}</span></a></div>
                </div>
                <div class="user-body-bottom"><a href=""><img src="../assets/icon/user_payment.png"/></a> </div>
            </el-card>

        </div>
    </div>
</template>

<script>
    export default {
        name: "HomePage",
        data: function () {
            return {
                items: 5,
                bannerLabels: ["周年庆战利品大分享", "早秋女鞋精品", "超人气博主Emma开箱啦", "OL风怎么穿 全场6折", "打造您的专属品牌"],
                bannerHrefs: ["https://www.taobao.com", "https://www.jd.com", "https://www.taobao.com", "https://www.jd.com", "https://www.taobao.com"],
                banners: [require("../assets/banner/banner_1.jpg"), require("../assets/banner/banner_2.jpg"), require("../assets/banner/banner_3.jpg"), require("../assets/banner/banner_4.jpg"), require("../assets/banner/banner_5.jpg")],
                userLabels: [["最具美誉的跨境服务", "CEO邮箱直达"], ["7x24小时金牌客服", "一对一专家客服"], ["首创代购返利模式", "海量高返品牌"]],
                userHrefs: ["mailto:yuarchie@163.com", "null", ""],
            }
        },
        computed: {},
        methods: {}
    }
</script>

<style scoped>

    a:link, a:visited, a:hover {
        text-decoration: none;
    }

    .home-page {
        display: flex;
        width: 1190px;
        padding-top: 10px;
        margin: 0 auto;

    }

    .banner {
        width: 950px;
        height: 360px;
    }

    .user-header {
        display: inline-flex;
        align-items: center;
    }

    .user-header img {
        width: 50px;
        height: 50px;
    }

    .user-header span {
        font-size: 14px;
    }

    .user-header a {
        display: inline-block;
        width: 50px;
        height: 50px;
        margin: 0;
    }

    .user-header dl {
        display: inline-block;
        margin: 0 0 0 10px;
    }

    .user-info {
        width: 230px;
        margin-left: 10px;
    }

    .user-body-item {
        display: list-item;
        margin: 10px;
        padding: 5px;
        background: #5e75e2;
    }

    .user-body-item span {
        font-size: 12px;
        color: #fff;
    }

    .user-body-item a span {
        font-size: 12px;
        color: #ffe3d7;
    }

    .user-body-header {

        padding: 10px 10px 0 10px;
    }

    .user-body-header a {
        width: 100%;
        display: inline;
    }

    .user-body-header a span {
        color: #fff;
        font-size: 14px;
        font-weight: bold;
    }

    .user-body-header a span::after {
        content: url("../assets/icon/icon_right_white_16.png");
        float: right;
        margin-top: 5px;
    }

    .user-body-header a img {
        margin: 0 auto;
    }

    .user-body-bottom {
        border-top: #e3ebf2 solid  1px;
        margin: 10px;
        padding-top: 10px;
    }


</style>
