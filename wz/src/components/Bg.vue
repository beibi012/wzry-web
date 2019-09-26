<template>
    <div id="bg">
      <div class="header-nav" @mouseenter="subnavEnter" @mouseleave="subnavLeave">
        <div class="main-nav">
          <a href=""><img class="wz-logo" src="../../images/wz-logo.png" /></a>
          <ul class="ul-nav clearfix"> <!-- @mouseenter="navliEnter" @mouseleave="navliLeave"-->
            <li v-for="(value,name,index) in items" @mouseenter="navliEnter(index)" @mouseleave="navliLeave">
              <a href="" class="nav-li" :class="index==match?'nav-change':''">{{value}}<em>{{name}}</em></a>
            </li>
          </ul>
          <div class="login-pannel">
            <a href=""><img class="login-img" src="../../images/header-nav.png"/></a>
            <a class="login-a" href="">登陆游戏</a>
            <p class="login-p">登陆后查看游戏战绩</p>
          </div>
        </div>
          <div class="sub-nav"  :class="subnav_show"><!--v-show="subnav_show"-->
            <ul class="sub-nav-inner">
              <li class="down-nav"></li>
              <li class="down-nav">
              <a href="" v-for="value in data_li">{{value}}</a>
            </li>
              <li class="down-nav">
                <a href="" v-for="value in content_li">{{value}}</a>
              </li>
              <li class="down-nav">
                <a href="" v-for="value in match_li">{{value}}</a>
              </li>
              <li class="down-nav">
                <a href="" v-for="value in culture_li">{{value}}</a>
              </li>
              <li class="down-nav">
                <a href="" v-for="value in community_li">{{value}}</a>
              </li>
              <li class="down-nav">
                <a href="" v-for="value in player_li">{{value}}</a>
              </li>
            </ul>
          </div>
        </div>
      <div class="main_top">
        <div class="r-box">
        <div class="rotate">
          <ul class="r-ul" :class="rstyle" >
            <li v-for="(title) in titles" ><a href=""><img :src="title.img" /></a></li>
          </ul>
        </div>
        <div class="r-title" >
          <span class="rt" v-for="(title,i) in titles" :class="{rn:rtn===i}"
                @mouseenter="titleEnter(i,title)" >{{title.name}}</span>
        </div>
        </div>
        <div class="news_container">
          <div class="news_title">
            <ul>
              <li v-for="(value,name,newsindex) in newstitles"  @mouseenter="newstitleEnter(newsindex)"
                  :class="newstitle_match===newsindex?'title_change':''">
                <a href="">{{value}}</a></li>
              <li><a href="">...</a></li>
              </ul>

          </div>
          <div class="news_content">
            <div class="news_content_container" :class="newscontent_change">
              <ul class="news1">
                <li class="line_sp"><a class="news1_txt" href="">0花好月圆 中秋佳节福利活动周开启</a></li>
                <li><a class="news1_txt" href="">9月10日全服不停机更新公告</a><em>09/09</em></li>
                <li><a class="news1_txt" href="">99公益日，王者峡谷“益”起来</a><em>09/09</em></li>
                <li><a class="news1_txt" href="">吕布新秀歌曲《断戟的约定》上线，视频创作大赛邀你参与！</a><em>09/09</em></li>
                <li><a class="news1_txt" href="">9月7日体验服停机更新公告</a><em>09/09</em></li>
                <li><a class="news1_txt" href="">Pick Me | 喊出我的新皮肤名字~“无限星赏官！”</a><em>09/09</em></li>
                <li><a class="news1_txt" href="">【预告】峡谷益起做好事 拿专属头像框活动公告</a><em>09/09</em></li>
                <li><a class="news1_txt" href="">周年庆版本爆料①  全新野怪、边路改造、视野新体验...王者峡谷2.0+大揭秘！</a><em>09/09</em></li>
              </ul>
              <ul class="news1">
                <li class="line_sp"><a class="news1_txt" href="">1花好月圆 中秋佳节福利活动周开启</a></li>
                <li><a class="news1_txt" href="">周年庆版本爆料② | 装备、技能、野怪现已加入特效套餐！</a><em>09/09</em></li>
                <li><a class="news1_txt" href="">周年庆版本爆料② | 装备、技能、野怪现已加入特效套餐！</a><em>09/09</em></li>
                <li><a class="news1_txt" href="">周年庆版本爆料② | 装备、技能、野怪现已加入特效套餐！</a><em>09/09</em></li>
                <li><a class="news1_txt" href="">周年庆版本爆料② | 装备、技能、野怪现已加入特效套餐！</a><em>09/09</em></li>
                <li><a class="news1_txt" href="">周年庆版本爆料② | 装备、技能、野怪现已加入特效套餐！</a><em>09/09</em></li>
                <li><a class="news1_txt" href="">周年庆版本爆料② | 装备、技能、野怪现已加入特效套餐！</a><em>09/09</em></li>
                <li><a class="news1_txt" href="">周年庆版本爆料①  全新野怪、边路改造、视野新体验...王者峡谷2.0+大揭秘！</a><em>09/09</em></li>
              </ul>
              <ul class="news1">
                <li class="line_sp"><a class="news1_txt" href="">2花好月圆 中秋佳节福利活动周开启</a></li>
                <li><a class="news1_txt" href="">吕布新秀歌曲《断戟的约定》上线，视频创作大赛邀你参与！</a><em>09/09</em></li>
                <li><a class="news1_txt" href="">吕布新秀歌曲《断戟的约定》上线，视频创作大赛邀你参与！</a><em>09/09</em></li>
                <li><a class="news1_txt" href="">吕布新秀歌曲《断戟的约定》上线，视频创作大赛邀你参与！</a><em>09/09</em></li>
                <li><a class="news1_txt" href="">9月7日体验服停机更新公告</a><em>09/09</em></li>
                <li><a class="news1_txt" href="">吕布新秀歌曲《断戟的约定》上线，视频创作大赛邀你参与！</a><em>09/09</em></li>
                <li><a class="news1_txt" href="">【预告】峡谷益起做好事 拿专属头像框活动公告</a><em>09/09</em></li>
                <li><a class="news1_txt" href="">2周年庆版本爆料①  全新野怪、边路改造、视野新体验...王者峡谷2.0+大揭秘！</a><em>09/09</em></li>
              </ul>
              <ul class="news1">
                <li class="line_sp"><a class="news1_txt" href="">3花好月圆 中秋佳节福利活动周开启</a></li>
                <li><a class="news1_txt" href="">【预告】峡谷益起做好事 拿专属头像框活动公告</a><em>09/09</em></li>
                <li><a class="news1_txt" href="">【预告】峡谷益起做好事 拿专属头像框活动公告</a><em>09/09</em></li>
                <li><a class="news1_txt" href="">吕布新秀歌曲《断戟的约定》上线，视频创作大赛邀你参与！</a><em>09/09</em></li>
                <li><a class="news1_txt" href="">9月7日体验服停机更新公告</a><em>09/09</em></li>
                <li><a class="news1_txt" href="">Pick Me | 喊出我的新皮肤名字~“无限星赏官！”</a><em>09/09</em></li>
                <li><a class="news1_txt" href="">【预告】峡谷益起做好事 拿专属头像框活动公告</a><em>09/09</em></li>
                <li><a class="news1_txt" href="">3周年庆版本爆料①  全新野怪、边路改造、视野新体验...王者峡谷2.0+大揭秘！</a><em>09/09</em></li>
              </ul>
              <ul class="news1">
                <li class="line_sp"><a class="news1_txt" href="">4花好月圆 中秋佳节福利活动周开启</a></li>
                <li><a class="news1_txt" href="">9月10日全服不停机更新公告</a><em>09/09</em></li>
                <li><a class="news1_txt" href="">9公益日，王者峡谷“益”起来</a><em>09/09</em></li>
                <li><a class="news1_txt" href="">吕布新秀歌曲《断戟的约定》上线，视频创作大赛邀你参与！</a><em>09/09</em></li>
                <li><a class="news1_txt" href="">9月7日体验服停机更新公告</a><em>09/09</em></li>
                <li><a class="news1_txt" href="">Pick Me | 喊出我的新皮肤名字~“无限星赏官！”</a><em>09/09</em></li>
                <li><a class="news1_txt" href="">【预告】峡谷益起做好事 拿专属头像框活动公告</a><em>09/09</em></li>
                <li><a class="news1_txt" href="">周年庆版本爆料①  全新野怪、边路改造、视野新体验...王者峡谷2.0+大揭秘！</a><em>09/09</em></li>
              </ul>
            </div>
          </div>


        </div>
        <div class="download">
          <a href="" class="download_btn"></a>
          <a href="" class="guard_btn"></a>
          <a href="" class="tiyan_btn"></a>
        </div>
      </div>
      <div class="quick_entrance">
        <a href=""><img src="../../images/q1.png" /></a>
        <a href=""><img src="../../images/q2.jpg" /></a>
        <a href=""><img src="../../images/q3.jpg" /></a>
        <a href=""><img src="../../images/q4.jpg" /></a>
      </div>
    </div>
</template>

<script>
    export default {
        name: "Bg",
        data(){
            return{
                rtn:0,
                rstyle:'r-0',
                match:-1,
                subnav_show:'',
                newscontent_change:'news_content0',
                newstitle_match:0,
                items:{
                    HOME:'官网首页',
                    DATA:'游戏资料',
                    CONTENTS:'内容中心',
                    MATCH:'赛事中心',
                    CULTURE:'百态王者',
                    COMMUNITY:'社区互动',
                    PLAYER:'玩家支持'
                },
                titles:[
                    {name:'秋季赛11日开战', img:'static/r1.jpeg',style:'r-0'},
                    {name:'每周优质内容盘点', img:'static/r2.jpeg',style:'r-1'},
                    {name:'美少女转会危机', img:'static/r3.jpeg',style:'r-2'},
                    {name:'完美克制虞姬', img:'static/r4.jpeg',style:'r-3'},
                    {name:'欧皇克星马孟起', img:'static/r5.jpeg',style:'r-4'}
                ],
                newstitles:{
                    name1:'热门',
                    name2:'新闻',
                    name3:'公告',
                    name4:'活动',
                    name5:'赛事',
                },
                data_li:{a1:'版本介绍',a2:'游戏介绍',a3:'英雄资料',a4:'爆料站',a5:'故事站',a6:'游戏壁纸',},
                content_li:{a1:'攻略中心',a2:'英雄攻略',a3:'视频中心',a4:'王者视角',a5:'作者入驻',a6:'媒体入驻',},
                match_li:{a1:'冠军杯',a2:'KPL',a3:'KPKPL',a4:'高校赛',a5:'城市赛',a6:'全民赛',a7:'赛事数据',},
                culture_li:{a1:'荣耀传承',a2:'王者文化站',a3:'王者音乐听',a4:'万千世界',a5:'星光殿堂',a6:'商户特权',},
                community_li:{a1:'王者互动',a2:'手Q部落',a3:'微信圈子',a4:'官方微博',a5:'微信公众号',a6:'手Q订阅号',a7:'同人社区',},
                player_li:{a1:'成长守护平台',a2:'健康系统',a3:'狄仁杰护卫站',a4:'客服专区',a5:'礼包兑换',a6:'自助服务',},
            }
        },
        watch:{
            newstitle_match(n){
                if(n===1){
                    this.newscontent_change='news_content1'
                }else if(n===2){
                    this.newscontent_change='news_content2'
                }else if(n===3){
                    this.newscontent_change='news_content3'
                }else if(n===4){
                    this.newscontent_change='news_content4'
                }else{
                    this.newscontent_change='news_content0'
                }
            }
    },
        methods:{
            subnavEnter(){
                this.subnav_show='sub-nav-enter';
            },
            subnavLeave(){
                this.subnav_show='sub-nav-leave';
            },
            navliEnter(index){
                this.match=index;
            },
            navliLeave(){
                this.match=-1;
            },
            titleEnter(i,title){
                this.rtn=i;
                this.rstyle=title.style;
            },
            newstitleEnter(newsindex){
                this.newstitle_match=newsindex;
            }

        },
        mounted() {
            setInterval(()=>{
                ++this.rtn;
                if(this.rtn > this.titles.length-1) this.rtn=0;
                this.rstyle=this.titles[this.rtn].style;
            },5000)
        }
    }
</script>

<style scoped>

</style>
