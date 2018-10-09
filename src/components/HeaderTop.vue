<template>
    <div class="header-top">
        <div class="header-top-main">
            <el-row type="flex" justify="start" align="middle">
                <el-col class="col" :span="3">
                    <i id="header-icon-global"></i>
                    <el-dropdown :hide-on-click="false" @visible-change="reduction">
                        <span class="el-dropdown-link">{{radio1+"/ "+radio2}}<i
                                class="el-icon-arrow-down"></i></span>
                        <el-dropdown-menu slot="dropdown">
                            <el-dropdown-item disabled>
                                <span>请选择语言</span>
                            </el-dropdown-item>
                            <el-dropdown-item>
                                <el-radio-group v-model="radio1" size="small">
                                    <el-radio-button v-bind:label="chinese"/>
                                    <el-radio-button v-bind:label="english"/>
                                </el-radio-group>
                            </el-dropdown-item>
                            <el-dropdown-item disabled>
                                <span>请选择币种</span>
                            </el-dropdown-item>
                            <el-dropdown-item>
                                <el-radio-group v-model="radio2" size="small">
                                    <el-radio-button v-bind:label="rmb"/>
                                    <el-radio-button v-bind:label="dollar"/>
                                </el-radio-group>
                            </el-dropdown-item>
                            <el-dropdown-item divided command="a">
                                <el-button id="ok" size="mini" type="primary">确定</el-button>
                            </el-dropdown-item>
                        </el-dropdown-menu>
                    </el-dropdown>
                </el-col>
                <el-col class="col" :span="9">
                    <span>{{datetime}}</span>
                </el-col>
                <el-col class="col" :span="5">
                    <span class="clock">欢迎</span>
                    <a class="clock"
                       href="//login.superbuy.com/cn/page/login/?ref=https%3A%2F%2Fwww.superbuy.com%2Fcn%2F">登陆</a>
                    <span class="clock">或</span>
                    <el-tooltip class="clock" effect="dark" content="CN ￥188" placement="right">
                        <a href="//login.superbuy.com/cn/page/login/?ref=https%3A%2F%2Fwww.superbuy.com%2Fcn%2F">注册</a>
                    </el-tooltip>

                </el-col>
                <el-col class="col" :span="2">
                    <el-dropdown>
                        <span class="el-dropdown-link">我的superbuy<i class="el-icon-arrow-down"></i></span>
                        <el-dropdown-menu slot="dropdown">
                            <el-dropdown-item>购物订单</el-dropdown-item>
                            <el-dropdown-item>转运订单</el-dropdown-item>
                            <el-dropdown-item>我的仓库</el-dropdown-item>
                            <el-dropdown-item>我的包裹</el-dropdown-item>
                            <el-dropdown-item>我的推广联盟</el-dropdown-item>
                        </el-dropdown-menu>
                    </el-dropdown>
                </el-col>
                <el-col class="col" :span="2">
                    <el-dropdown>
                        <span class="el-dropdown-link">商业客户<i class="el-icon-arrow-down"></i></span>
                        <el-dropdown-menu slot="dropdown">
                            <el-dropdown-item>商业服务</el-dropdown-item>
                            <el-dropdown-item>企业购</el-dropdown-item>
                            <el-dropdown-item>推广联盟</el-dropdown-item>
                            <el-dropdown-item>全球合伙人</el-dropdown-item>
                            <el-dropdown-item>1688代购</el-dropdown-item>
                        </el-dropdown-menu>
                    </el-dropdown>
                </el-col>
                <el-col class="col" :span="1">
                    <el-dropdown>
                        <i id="header-icon-tools"></i>
                        <el-dropdown-menu slot="dropdown">
                            <el-dropdown-item>购物助手</el-dropdown-item>
                            <el-dropdown-item>运费估算</el-dropdown-item>
                            <el-dropdown-item>物流查询</el-dropdown-item>
                            <el-dropdown-item>支付方式</el-dropdown-item>
                        </el-dropdown-menu>
                    </el-dropdown>
                </el-col>
                <el-col class="col" :span="1">
                    <el-dropdown>
                        <i id="header-icon-service"></i>
                        <el-dropdown-menu slot="dropdown">
                            <el-dropdown-item>帮助中心</el-dropdown-item>
                            <el-dropdown-item>消费者客服</el-dropdown-item>
                            <el-dropdown-item>商业合作</el-dropdown-item>
                        </el-dropdown-menu>
                    </el-dropdown>
                </el-col>
                <el-col class="col" :span="1">
                    <el-dropdown>
                        <i id="header-icon-app"></i>
                        <el-dropdown-menu slot="dropdown">
                            <el-dropdown-item>购物助手</el-dropdown-item>
                        </el-dropdown-menu>
                    </el-dropdown>
                </el-col>
            </el-row>
        </div>
    </div>
</template>

<script>
    const languages = ["中文（简体）", "English"];
    const currencies = ["CN ￥", "US $"];

    export default {
        name: "HeaderTopMain",
        data: function () {
            return {
                chinese: languages[0],
                english: languages[1],
                rmb: currencies[0],
                dollar: currencies[1],
                radio1: languages[0],
                radio2: currencies[0],
                datetime: "北京时间 " + new Date().toLocaleString("zh-CN")
            }
        },
        mounted() {
            this.updateTime()
        },
        methods: {
            reduction(b) {
                if (!b) {
                    this.radio1 = languages[0];
                    this.radio2 = currencies[0];
                }
            },
            updateTime() {
                setInterval(this.time, 1000)
            },
            time() {
                this.datetime = "北京时间 " + new Date().toLocaleString("zh-CN");
            }
        }
    }


</script>

<style scoped>

    a:link, a:visited {
        text-decoration: none;
    }

    a:hover {
        text-decoration: underline;
    }

    .col {
        display: flex;
        display: -webkit-flex;
        align-items: center;
        height: 30px;
    }

    .header-top {
        min-width: 1190px;
        background: #fbfbfb;
        border-bottom: 1px solid #eee;
    }

    .header-top-main {
        font-size: 12px;
        color: #666666;
        width: 1190px;
        margin: 0 auto;
    }

    .el-dropdown-link {
        font-size: 12px;
        cursor: pointer;
    }

    .el-icon-arrow-down {
        font-size: 2px;
    }

    .clock {
        display: inline-block;
        height: 30px;
        line-height: 30px;
        margin: 0 4px;
    }

    span, a {
        font-size: 12px;
    }

    .el-icon-setting {
        font-size: 16px;
    }

    a {
        color: #1268bb;
        text-decoration: none;
        cursor: pointer;
    }

    #header-icon-tools {
        display: block;
        float: right;
        width: 30px;
        height: 30px;
        background: url("../assets/icon/header_icon_tools.png");
    }

    #header-icon-service {
        display: block;
        float: right;
        width: 30px;
        height: 30px;
        background: url("../assets/icon/header_icon_service.png");
    }

    #header-icon-app {
        display: block;
        float: right;
        width: 30px;
        height: 30px;
        background: url("../assets/icon/header_icon_app.png");
    }

    #header-icon-global {
        margin-right: 2px;
        width: 15px;
        height: 15px;
        background: url("../assets/icon/header_icon_global.png");
    }

    #ok {
        float: right;
    }


</style>
