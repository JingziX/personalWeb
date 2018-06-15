<template>
    <div class="wrapper" style="background:#fff;">
        <div class="login-box" v-show="!isLogin">
            <div class="btn-box">
                <span class="btn" @click="loginFun">登录</span>
            </div>
        </div>
        <template v-show="isLogin">
            <!-- <img src="../images/img2.jpg" alt=""> -->
            <div class="index-title">
                我如果爱你——</br>
                绝不像攀援的凌霄花，
                借你的高枝炫耀自己；</br>
                我如果爱你——</br>
                绝不学痴情的鸟儿，
                为绿荫重复单调的歌曲；
            </div>
            <ul class="nav-list">
                <li class="nav-item" v-for="(item,index) in titleList" :key="item.type" @click="toDetail">
                    <div class="nav-item-content">
                        {{item.content}}
                    </div>
                </li>
            </ul>
        </template>
    </div>
</template>
<script>
export default {
    name: 'navigation',
    data() {
        return {
            msg: 'Welcome,my friend',
            isLogin:false,
            titleList:[{
                type:1,
                content:"TF黑管"
            },{
                type:2,
                content:"YSL圆管"
            },{
                type:3,
                content:"迪奥烈艳蓝"
            },{
                type:4,
                content:"纪梵希小羊皮"
            },{
                type:5,
                content:"娇兰kisskiss黑管娇兰kisskiss黑管"
            },{
                type:6,
                content:"雅诗兰黛唇膏"
            },{
                type:7,
                content:"香奈儿丝绒"
            },{
                type:8,
                content:"魅可子弹头"
            },{
                type:9,
                content:"雅诗兰黛唇膏"
            },{
                type:10,
                content:"香奈儿丝绒"
            },{
                type:11,
                content:"魅可子弹头"
            },{
                type:12,
                content:"纪梵希小羊皮"
            }]
        }
    },
    methods:{
        toDetail(){
            
        },
        loginFun(){
            this.isLogin = true;
        }
    }
}
</script>