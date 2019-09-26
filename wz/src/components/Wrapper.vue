<template>
    <div id="wrapper">
      <div class="wrapper_content">
        <div class="content_center">
          <div class="content_header">
            <h3 class="content_title">内容中心</h3>
            <a href="" class="more_btn">更多</a>
          </div>
          <div class="content_subnav">
            <a href="" @mouseenter="c1Enter" :class="{on:c1===true}">精品栏目</a>
            <a href="" @mouseenter="c2Enter" :class="{on:c2===true}">赛事精品</a>
            <a href="" @mouseenter="c3Enter" :class="{on:c3===true}">英雄攻略</a>
          </div>


          <transition name="cc">
            <div class="content1 ct" v-show="c1">
              <div class="c_title">
                <a href="" v-for="(value,name,index) in c1_title" :class="{on:c_match===index}" @mouseenter="c_titleEnter(index)">{{value}}</a>
              </div>
              <div class="c_content">
                <ul class="content_list">
                  <li class="content_li" v-for="element in c_content">
                    <a href="">
                      <img :src="'static/'+element.img+'.jpg'" height="125" width="209"/>
                      <p class="content_tit">{{element.text}}</p>
                      <p class="content_bt"><em class="vl">{{element.number}}</em><em class="vr">{{element.date}}</em></p>
                      <div class="mask"><span class="button_img"></span></div>
                    </a>
                  </li>
                </ul>
              </div>
            </div>
          </transition>


          <transition name="cc">
            <div class="content2 ct" v-show="c2">
              <div class="c_title">
                <a href="" v-for="(value,name,index) in c1_title" :class="{on:c_match===index}" @mouseenter="c_titleEnter(index)">{{value}}</a>
              </div>
              <div class="c_content">
                <ul class="content_list">
                  <li class="content_li" v-for="element in c_content">
                    <a href="">
                      <img :src="'static/'+element.img+'.jpg'" height="125" width="209"/>
                      <p class="content_tit">{{element.text}}</p>
                      <p class="content_bt"><em class="vl">{{element.number}}</em><em class="vr">{{element.date}}</em></p>
                      <div class="mask"><span class="button_img"></span></div>
                    </a>
                  </li>
                </ul>
              </div>
            </div>
          </transition>


          <transition name="cc">
            <div class="content3 ct" v-show="c3">
              <div class="c_title">
                <a href="" v-for="(value,name,index) in c1_title" :class="{on:c_match===index}" @mouseenter="c_titleEnter(index)">{{value}}</a>
              </div>
              <div class="c_content">
                <ul class="content_list">
                  <li class="content_li" v-for="element in c_content">
                    <a href="">
                      <img :src="'static/'+element.img+'.jpg'" height="125" width="209"/>
                      <p class="content_tit">{{element.text}}</p>
                      <p class="content_bt"><em class="vl">{{element.number}}</em><em class="vr">{{element.date}}</em></p>
                      <div class="mask"><span class="button_img"></span></div>
                    </a>
                  </li>
                </ul>
              </div>
            </div>
          </transition>


        </div>
        <div class="hero">
          <h3 class="hero_title">英雄/皮肤</h3>
          <div class="hero_subnav">
            <a href="" @mouseenter="h1Enter" :class="{on:h1===true}">最新英雄</a>
            <a href="" @mouseenter="h2Enter" :class="{on:h2===true}">最新皮肤</a>
            <a href="" @mouseenter="h3Enter" :class="{on:h3===true}">周免英雄</a>
          </div>
          <div class="h_container" :class="h_move">
              <div class="h1">
                <div class="new_hero">
                  <a href=""><img src="../../images/x_mc.jpg"/></a>
                  <div class="new_hero_bottom">
                    <p class="new_hero_name">新英雄：马超</p>
                    <p>上线时间：2019.08.15</p>
                  </div>
                </div>
                <div class="hero_list">
                  <ul>
                    <li><a href="">
                      <img src="../../images/x_y.jpg" />
                      <span class="mask"></span>
                      <span class="hero_name">曜</span>
                    </a></li>
                    <li><a href="">
                      <img src="../../images/x_yzj.jpg" />
                      <span class="mask"></span>
                      <span class="hero_name">云中君</span>
                    </a></li>
                    <li><a href="">
                      <img src="../../images/x_yy.jpg" />
                      <span class="mask"></span>
                      <span class="hero_name">瑶</span>
                    </a></li>
                    <li><a href="">
                      <img src="../../images/x_pg.jpg"/>
                      <span class="mask"></span>
                      <span class="hero_name">盘古</span>
                    </a></li>
                  </ul>
                </div>
              </div>
              <div class="h2">
                <div class="new_skin">
                  <a href=""><img src="../../images/x_gsl.jpg" /></a>
                  <div class="new_skin_bottom">
                    <p class="new_skin_name">新皮肤：公孙离-无限星赏官</p>
                    <p>上线时间：2019.09.10</p>
                  </div>
                </div>
                <div class="skin_list">
                  <ul>
                    <li><a href="">
                      <img src="../../images/x_smx.jpg"/>
                      <span class="mask"></span>
                      <span class="hero_name">沈梦溪-鲨炮海盗猫</span>
                    </a></li>
                    <li><a href="">
                      <img src="../../images/x_gj.jpg"/>
                      <span class="mask"></span>
                      <span class="hero_name">干将莫邪-久胜战神</span>
                    </a></li>
                    <li><a href="">
                      <img src="../../images/x_gjl.jpg"/>
                      <span class="mask"></span>
                      <span class="hero_name">高渐离-玩趣恶龙</span>
                    </a></li>
                    <li><a href="">
                      <img src="../../images/x_sb.jpg"/>
                      <span class="mask"></span>
                      <span class="hero_name">孙膑-归虚梦演</span>
                    </a></li>
                  </ul>
                </div>
              </div>
              <div class="h3">
                <div class="week_hero">
                  <ul>
                    <li><a href=""><img src="../../images/x_y.jpg"/>
                      <span class="mask"></span>
                      <span class="hero_name">曜</span></a></li>
                    <li><a href=""><img src="../../images/x_y.jpg"/>
                      <span class="mask"></span>
                      <span class="hero_name">曜</span></a></li>
                    <li><a href=""><img src="../../images/x_y.jpg"/>
                      <span class="mask"></span>
                      <span class="hero_name">曜</span></a></li>
                    <li><a href=""><img src="../../images/x_y.jpg"/>
                      <span class="mask"></span>
                      <span class="hero_name">曜</span></a></li>
                    <li><a href=""><img src="../../images/x_y.jpg"/>
                      <span class="mask"></span>
                      <span class="hero_name">曜</span></a></li>
                    <li><a href=""><img src="../../images/x_y.jpg"/>
                      <span class="mask"></span>
                      <span class="hero_name">曜</span></a></li>
                    <li><a href=""><img src="../../images/x_y.jpg"/>
                      <span class="mask"></span>
                      <span class="hero_name">曜</span></a></li>
                    <li><a href=""><img src="../../images/x_y.jpg"/>
                      <span class="mask"></span>
                      <span class="hero_name">曜</span></a></li>
                  </ul>
                </div>
              </div>
          </div>
        </div>
      </div>
      <div class="wrapper2">
        <div class="match_center">
          <div class="match_header">
            <h3 class="match_title">赛事中心</h3>
            <a href="" class="more_btn">更多</a>
          </div>
          <div class="match_subnav">
            <a href="" v-for="(value,name,index) in match_titlts" :class="{on:m_match===index}" @mouseenter="mEnter(index)">{{value}}<span></span></a>
          </div>
          <div class="match_content">
            <div class="match_news">
              <div class="match_img">
                <a href=""><img :src="'static/'+match_img+'.jpg'" /></a>
              </div>
              <div class="news_container">
                <ul class="news_list">
                  <li :class="{list_1:index===0}" v-for="(kpl,index) in match_type">
                    <span>{{kpl.type}}</span>
                    <a href="">{{kpl.a}}</a>
                    <em>{{kpl.date}}</em>
                    <a href="" v-if="index===0" class="a2">{{kpl.a}}</a>
                  </li>
                </ul>
              </div>
            </div>
            <div class="match_video">
              <ul class="video_list">
                <li class="video_li" v-for="element in m_content">
                  <a href="">
                    <img :src="'static/'+element.img+'.jpg'"/>
                    <p class="video_tit">{{element.text}}</p>
                    <p class="video_bt"><em class="vl">{{element.number}}</em><em class="vr">{{element.date}}</em></p>
                    <div class="mask"><span class="button_img"></span></div>
                  </a>
                </li>
              </ul>
            </div>
          </div>
        </div>
        <div class="match_schedule">
          <div class="sch_header">
            <h3 class="sch_title">KPL赛程</h3>
            <a href="" class="buy_ticket">购票</a>
            <a href="" class="more_btn">更多</a>
          </div>
          <div class="sch_subnav">
            <span class="col1">时间</span>
            <span class="col1">战队</span>
            <span class="col2"></span>
            <span class="col1">战队</span>
          </div>
          <div class="sch_content">
            <ul>
              <li v-for="vs in match_vs">
                <span class="match_time">{{vs.time}}</span>
                <span class="team_name"><img :src="'static/'+vs.img1+'.png'" alt="" class="team_icon"><em>{{vs.team1}}</em></span>
                <span class="vs">VS</span>
                <span class="team_name"><img :src="'static/'+vs.img2+'.png'" alt=""class="team_icon"><em>{{vs.team2}}</em></span>
              </li>
              <li></li>
              <li></li>
            </ul>
          </div>
          <div class="adver">
            <a href="">
              <img src="../../static/adver.jpg" height="159" width="293"/></a>
          </div>
        </div>

      </div>
    </div>
</template>

<script>
    export default {
        name: "Wrapper",
        data(){
            return{
                match_vs:[
                    {time:'9-11 15:00',team1:'XQ',team2:'TES',img1:'xq',img2:'tes'},
                    {time:'9-11 18:00',team1:'AG超玩会',team2:'QGhappy',img1:'ag',img2:'qg'},
                    {time:'9-11 20:00',team1:'AS仙阁',team2:'estarPro',img1:'as',img2:'es'},
                    {time:'9-12 18:00',team1:'XQ',team2:'estarPro',img1:'xq',img2:'es'},
                    {time:'9-12 20:00',team1:'AS仙阁',team2:'QGhappy',img1:'as',img2:'qg'},

                ],
                m_content:[
                    {img:'k_v1',number:'1.8万',date:'2019-9-11',text:'王者荣耀世冠：远游之枪华丽收割，花满楼世冠马可波罗击杀集锦'},
                    {img:'k_v1',number:'1.8万',date:'2019-9-11',text:'王者荣耀世冠：远游之枪华丽收割，花满楼世冠马可波罗击杀集锦'},
                    {img:'k_v1',number:'1.8万',date:'2019-9-11',text:'王者荣耀世冠：远游之枪华丽收割，花满楼世冠马可波罗击杀集锦'},
                    {img:'k_v1',number:'1.8万',date:'2019-9-11',text:'王者荣耀世冠：远游之枪华丽收割，花满楼世冠马可波罗击杀集锦'},
                    {img:'k_v1',number:'1.8万',date:'2019-9-11',text:'王者荣耀世冠：远游之枪华丽收割，花满楼世冠马可波罗击杀集锦'},
                    {img:'k_v1',number:'1.8万',date:'2019-9-11',text:'王者荣耀世冠：远游之枪华丽收割，花满楼世冠马可波罗击杀集锦'},
                    {img:'k_v1',number:'1.8万',date:'2019-9-11',text:'王者荣耀世冠：远游之枪华丽收割，花满楼世冠马可波罗击杀集锦'},
                    {img:'k_v1',number:'1.8万',date:'2019-9-11',text:'王者荣耀世冠：远游之枪华丽收割，花满楼世冠马可波罗击杀集锦'},
                ],
                m_content1:[
                    {img:'k_v1',number:'1.8万',date:'2019-9-11',text:'王者荣耀世冠：远游之枪华丽收割，花满楼世冠马可波罗击杀集锦'},
                    {img:'k_v1',number:'1.8万',date:'2019-9-11',text:'王者荣耀世冠：远游之枪华丽收割，花满楼世冠马可波罗击杀集锦'},
                    {img:'k_v1',number:'1.8万',date:'2019-9-11',text:'王者荣耀世冠：远游之枪华丽收割，花满楼世冠马可波罗击杀集锦'},
                    {img:'k_v1',number:'1.8万',date:'2019-9-11',text:'王者荣耀世冠：远游之枪华丽收割，花满楼世冠马可波罗击杀集锦'},
                    {img:'k_v1',number:'1.8万',date:'2019-9-11',text:'王者荣耀世冠：远游之枪华丽收割，花满楼世冠马可波罗击杀集锦'},
                    {img:'k_v1',number:'1.8万',date:'2019-9-11',text:'王者荣耀世冠：远游之枪华丽收割，花满楼世冠马可波罗击杀集锦'},
                    {img:'k_v1',number:'1.8万',date:'2019-9-11',text:'王者荣耀世冠：远游之枪华丽收割，花满楼世冠马可波罗击杀集锦'},
                    {img:'k_v1',number:'1.8万',date:'2019-9-11',text:'王者荣耀世冠：远游之枪华丽收割，花满楼世冠马可波罗击杀集锦'},
                ],
                match_titlts:{
                    kpl:'KPL职业联赛',
                    kcc:'KCC世界冠军杯',
                    kpkpl:'KRKPL职业联赛',
                    koc:'KOC王者城市赛',
                    gxs:'王者高校联赛',
                    tga:'TGA大奖赛',
                    wgi:'微信游戏邀请赛',
                },
                list_1:'list_1',
                c1:true,
                c2:false,
                c3:false,
                on:'on',
                h1:true,
                h2:false,
                h3:false,
                c_match:0,
                m_match:0,
                match_type:[],
                match_img:'kpl',
                h_move:'h_move1',
                c1_title:{
                    t1:'最新',
                    t2:'百星王者带你飞',
                    t3:'峡谷情报局',
                    t4:'零度王者视角',
                },
                c_content:[
                    {img:'c_c1',number:'1.8万',date:'2019-9-11',text:'【王者克制论】扼杀马超骚走位 枪王折戟秒成渣'},
                    {img:'c_c1',number:'1.8万',date:'2019-9-11',text:'【王者克制论】扼杀马超骚走位 枪王折戟秒成渣'},
                    {img:'c_c1',number:'1.8万',date:'2019-9-11',text:'【王者克制论】扼杀马超骚走位 枪王折戟秒成渣'},
                    {img:'c_c1',number:'1.8万',date:'2019-9-11',text:'【王者克制论】扼杀马超骚走位 枪王折戟秒成渣'},
                    {img:'c_c8',number:'1.8万',date:'2019-9-11',text:'【王者克制论】扼杀马超骚走位 枪王折戟秒成渣'},
                    {img:'c_c8',number:'1.8万',date:'2019-9-11',text:'【王者克制论】扼杀马超骚走位 枪王折戟秒成渣'},
                    {img:'c_c8',number:'1.8万',date:'2019-9-11',text:'【王者克制论】扼杀马超骚走位 枪王折戟秒成渣'},
                    {img:'c_c8',number:'1.8万',date:'2019-9-11',text:'【王者克制论】扼杀马超骚走位 枪王折戟秒成渣'}
                ],
                c_content0:[
                    {img:'c_c1',number:'1.8万',date:'2019-9-11',text:'【王者克制论】扼杀马超骚走位 枪王折戟秒成渣'},
                    {img:'c_c1',number:'1.8万',date:'2019-9-11',text:'【王者克制论】扼杀马超骚走位 枪王折戟秒成渣'},
                    {img:'c_c1',number:'1.8万',date:'2019-9-11',text:'【王者克制论】扼杀马超骚走位 枪王折戟秒成渣'},
                    {img:'c_c1',number:'1.8万',date:'2019-9-11',text:'【王者克制论】扼杀马超骚走位 枪王折戟秒成渣'},
                    {img:'c_c8',number:'1.8万',date:'2019-9-11',text:'【王者克制论】扼杀马超骚走位 枪王折戟秒成渣'},
                    {img:'c_c8',number:'1.8万',date:'2019-9-11',text:'【王者克制论】扼杀马超骚走位 枪王折戟秒成渣'},
                    {img:'c_c8',number:'1.8万',date:'2019-9-11',text:'【王者克制论】扼杀马超骚走位 枪王折戟秒成渣'},
                    {img:'c_c8',number:'1.8万',date:'2019-9-11',text:'【王者克制论】扼杀马超骚走位 枪王折戟秒成渣'}
                ],
                c_content1:[
                    {img:'c_c2',number:'1.8万',date:'2019-9-11',text:'【峡谷情报局】第78期：暗影刀锋杀人无形，隐匿突袭出奇制胜'},
                    {img:'c_c2',number:'1.8万',date:'2019-9-11',text:'【峡谷情报局】第78期：暗影刀锋杀人无形，隐匿突袭出奇制胜'},
                    {img:'c_c2',number:'1.8万',date:'2019-9-11',text:'【峡谷情报局】第78期：暗影刀锋杀人无形，隐匿突袭出奇制胜'},
                    {img:'c_c2',number:'1.8万',date:'2019-9-11',text:'【峡谷情报局】第78期：暗影刀锋杀人无形，隐匿突袭出奇制胜'},
                    {img:'c_c7',number:'1.8万',date:'2019-9-11',text:'【峡谷情报局】第78期：暗影刀锋杀人无形，隐匿突袭出奇制胜'},
                    {img:'c_c7',number:'1.8万',date:'2019-9-11',text:'【峡谷情报局】第78期：暗影刀锋杀人无形，隐匿突袭出奇制胜'},
                    {img:'c_c7',number:'1.8万',date:'2019-9-11',text:'【峡谷情报局】第78期：暗影刀锋杀人无形，隐匿突袭出奇制胜'},
                    {img:'c_c7',number:'1.8万',date:'2019-9-11',text:'【峡谷情报局】第78期：暗影刀锋杀人无形，隐匿突袭出奇制胜'}
                ],
                c_content2:[
                    {img:'c_c3',number:'1.8万',date:'2019-9-11',text:'【百星王者带你飞】103期：沈梦溪的暴躁节奏，炸翻峡谷喵计划'},
                    {img:'c_c4',number:'1.8万',date:'2019-9-11',text:'【百星王者带你飞】103期：沈梦溪的暴躁节奏，炸翻峡谷喵计划'},
                    {img:'c_c5',number:'1.8万',date:'2019-9-11',text:'【百星王者带你飞】103期：沈梦溪的暴躁节奏，炸翻峡谷喵计划'},
                    {img:'c_c6',number:'1.8万',date:'2019-9-11',text:'【百星王者带你飞】103期：沈梦溪的暴躁节奏，炸翻峡谷喵计划'},
                    {img:'c_c3',number:'1.8万',date:'2019-9-11',text:'【百星王者带你飞】103期：沈梦溪的暴躁节奏，炸翻峡谷喵计划'},
                    {img:'c_c4',number:'1.8万',date:'2019-9-11',text:'【百星王者带你飞】103期：沈梦溪的暴躁节奏，炸翻峡谷喵计划'},
                    {img:'c_c5',number:'1.8万',date:'2019-9-11',text:'【百星王者带你飞】103期：沈梦溪的暴躁节奏，炸翻峡谷喵计划'},
                    {img:'c_c6',number:'1.8万',date:'2019-9-11',text:'【百星王者带你飞】103期：沈梦溪的暴躁节奏，炸翻峡谷喵计划'}
                ],
                c_content3:[
                    {img:'c_c2',number:'1.8万',date:'2019-9-11',text:'【峡谷情报局】第78期：暗影刀锋杀人无形，隐匿突袭出奇制胜'},
                    {img:'c_c2',number:'1.8万',date:'2019-9-11',text:'【峡谷情报局】第78期：暗影刀锋杀人无形，隐匿突袭出奇制胜'},
                    {img:'c_c2',number:'1.8万',date:'2019-9-11',text:'【峡谷情报局】第78期：暗影刀锋杀人无形，隐匿突袭出奇制胜'},
                    {img:'c_c2',number:'1.8万',date:'2019-9-11',text:'【峡谷情报局】第78期：暗影刀锋杀人无形，隐匿突袭出奇制胜'},
                    {img:'c_c7',number:'1.8万',date:'2019-9-11',text:'【峡谷情报局】第78期：暗影刀锋杀人无形，隐匿突袭出奇制胜'},
                    {img:'c_c7',number:'1.8万',date:'2019-9-11',text:'【峡谷情报局】第78期：暗影刀锋杀人无形，隐匿突袭出奇制胜'},
                    {img:'c_c7',number:'1.8万',date:'2019-9-11',text:'【峡谷情报局】第78期：暗影刀锋杀人无形，隐匿突袭出奇制胜'},
                    {img:'c_c7',number:'1.8万',date:'2019-9-11',text:'【峡谷情报局】第78期：暗影刀锋杀人无形，隐匿突袭出奇制胜'}
                ],
                match_kpl:[
                    {type:'KPL',a:'秋季赛快讯：GK新老混打零封WE迎赛季首胜，鹏鹏射手表现出众双局最佳',date:'09-11'},
                    {type:'KPL',a:'秋季赛快讯：GK新老混打零封WE迎赛季首胜，鹏鹏射手表现出众双局最佳',date:'09-11'},
                    {type:'KPL',a:'秋季赛快讯：GK新老混打零封WE迎赛季首胜，鹏鹏射手表现出众双局最佳',date:'09-11'},
                    {type:'KPL',a:'秋季赛快讯：GK新老混打零封WE迎赛季首胜，鹏鹏射手表现出众双局最佳',date:'09-11'},
                    {type:'KPL',a:'秋季赛快讯：GK新老混打零封WE迎赛季首胜，鹏鹏射手表现出众双局最佳',date:'09-11'},
                    {type:'KPL',a:'秋季赛快讯：GK新老混打零封WE迎赛季首胜，鹏鹏射手表现出众双局最佳',date:'09-11'},
                    {type:'KPL',a:'秋季赛快讯：GK新老混打零封WE迎赛季首胜，鹏鹏射手表现出众双局最佳',date:'09-11'}
                ],
                match_kcc:[
                    {type:'KCC',a:'【关于王者荣耀赛事积分年与世冠名额获取规则调整公告】',date:'09-11'},
                    {type:'KCC',a:'【关于王者荣耀赛事积分年与世冠名额获取规则调整公告】',date:'09-11'},
                    {type:'KCC',a:'【关于王者荣耀赛事积分年与世冠名额获取规则调整公告】',date:'09-11'},
                    {type:'KCC',a:'【关于王者荣耀赛事积分年与世冠名额获取规则调整公告】',date:'09-11'},
                    {type:'KCC',a:'【关于王者荣耀赛事积分年与世冠名额获取规则调整公告】',date:'09-11'},
                    {type:'KCC',a:'【关于王者荣耀赛事积分年与世冠名额获取规则调整公告】',date:'09-11'},
                    {type:'KCC',a:'【关于王者荣耀赛事积分年与世冠名额获取规则调整公告】',date:'09-11'},

                ],
                match_kpkpl:[
                    {type:'KPKPL',a:'KRKPL秋季赛第二周前瞻：Nova、CW龙虎斗，VSG一胜难求？',date:'09-11'},
                    {type:'KPKPL',a:'KRKPL秋季赛第二周前瞻：Nova、CW龙虎斗，VSG一胜难求？',date:'09-11'},
                    {type:'KPKPL',a:'KRKPL秋季赛第二周前瞻：Nova、CW龙虎斗，VSG一胜难求？',date:'09-11'},
                    {type:'KPKPL',a:'KRKPL秋季赛第二周前瞻：Nova、CW龙虎斗，VSG一胜难求？',date:'09-11'},
                    {type:'KPKPL',a:'KRKPL秋季赛第二周前瞻：Nova、CW龙虎斗，VSG一胜难求？',date:'09-11'},
                    {type:'KPKPL',a:'KRKPL秋季赛第二周前瞻：Nova、CW龙虎斗，VSG一胜难求？',date:'09-11'},
                    {type:'KPKPL',a:'KRKPL秋季赛第二周前瞻：Nova、CW龙虎斗，VSG一胜难求？',date:'09-11'},

                ],
                match_koc:[
                    {type:'KOC',a:'第七届王者荣耀城市赛省赛深圳站 · 科技电竞，再燃热血！',date:'09-11'},
                    {type:'KOC',a:'第七届王者荣耀城市赛省赛深圳站 · 科技电竞，再燃热血！',date:'09-11'},
                    {type:'KOC',a:'第七届王者荣耀城市赛省赛深圳站 · 科技电竞，再燃热血！',date:'09-11'},
                    {type:'KOC',a:'第七届王者荣耀城市赛省赛深圳站 · 科技电竞，再燃热血！',date:'09-11'},
                    {type:'KOC',a:'第七届王者荣耀城市赛省赛深圳站 · 科技电竞，再燃热血！',date:'09-11'},
                    {type:'KOC',a:'第七届王者荣耀城市赛省赛深圳站 · 科技电竞，再燃热血！',date:'09-11'},
                    {type:'KOC',a:'第七届王者荣耀城市赛省赛深圳站 · 科技电竞，再燃热血！',date:'09-11'},

                ],
                match_gxs:[
                    {type:'高校赛',a:'触手可及的高校荣耀，第六届高校联赛线上赛道即将开启',date:'09-11'},
                    {type:'高校赛',a:'触手可及的高校荣耀，第六届高校联赛线上赛道即将开启',date:'09-11'},
                    {type:'高校赛',a:'触手可及的高校荣耀，第六届高校联赛线上赛道即将开启',date:'09-11'},
                    {type:'高校赛',a:'触手可及的高校荣耀，第六届高校联赛线上赛道即将开启',date:'09-11'},
                    {type:'高校赛',a:'触手可及的高校荣耀，第六届高校联赛线上赛道即将开启',date:'09-11'},
                    {type:'高校赛',a:'触手可及的高校荣耀，第六届高校联赛线上赛道即将开启',date:'09-11'},
                    {type:'高校赛',a:'触手可及的高校荣耀，第六届高校联赛线上赛道即将开启',date:'09-11'},
                ],
                match_tga:[
                    {type:'TGA',a:'【战报】王者荣耀4月第二周C组：公孙离岑中归月 DC战队顺利登顶',date:'09-11'},
                    {type:'TGA',a:'【战报】王者荣耀4月第二周C组：公孙离岑中归月 DC战队顺利登顶',date:'09-11'},
                    {type:'TGA',a:'【战报】王者荣耀4月第二周C组：公孙离岑中归月 DC战队顺利登顶',date:'09-11'},
                    {type:'TGA',a:'【战报】王者荣耀4月第二周C组：公孙离岑中归月 DC战队顺利登顶',date:'09-11'},
                    {type:'TGA',a:'【战报】王者荣耀4月第二周C组：公孙离岑中归月 DC战队顺利登顶',date:'09-11'},
                    {type:'TGA',a:'【战报】王者荣耀4月第二周C组：公孙离岑中归月 DC战队顺利登顶',date:'09-11'},
                    {type:'TGA',a:'【战报】王者荣耀4月第二周C组：公孙离岑中归月 DC战队顺利登顶',date:'09-11'},
                ],
                match_wgi:[
                    {type:'WGI',a:'坤音四子ONER率队决战峡谷，杨迪爆笑解说聚星之夜',date:'09-11'},
                    {type:'WGI',a:'坤音四子ONER率队决战峡谷，杨迪爆笑解说聚星之夜',date:'09-11'},
                    {type:'WGI',a:'坤音四子ONER率队决战峡谷，杨迪爆笑解说聚星之夜',date:'09-11'},
                    {type:'WGI',a:'坤音四子ONER率队决战峡谷，杨迪爆笑解说聚星之夜',date:'09-11'},
                    {type:'WGI',a:'坤音四子ONER率队决战峡谷，杨迪爆笑解说聚星之夜',date:'09-11'},
                    {type:'WGI',a:'坤音四子ONER率队决战峡谷，杨迪爆笑解说聚星之夜',date:'09-11'},
                    {type:'WGI',a:'坤音四子ONER率队决战峡谷，杨迪爆笑解说聚星之夜',date:'09-11'},
                ],

            }
        },
        methods:{
            c1Enter(){
                this.c1=true;
                this.c2=false;
                this.c3=false;
                this.c_match=0;
                this.c_content=this.c_content0;
            },
            c2Enter(){
                this.c1=false;
                this.c2=true;
                this.c3=false;
                this.c_match=0;
                this.c_content=this.c_content0;
            },
            c3Enter(){
                this.c1=false;
                this.c2=false;
                this.c3=true;
                this.c_match=0;
                this.c_content=this.c_content0;
            },
            h1Enter(){
                this.h1=true;
                this.h2=false;
                this.h3=false
                this.h_move='h_move1';
            },
            h2Enter(){
                this.h1=false;
                this.h2=true;
                this.h3=false
                this.h_move='h_move2';
            },
            h3Enter(){
                this.h1=false;
                this.h2=false;
                this.h3=true
                this.h_move='h_move3';
            },
            c_titleEnter(index){
                this.c_match=index;
                if(index===1){
                    this.c_content=this.c_content1;
                }else if(index===2){
                    this.c_content=this.c_content2;
                }else if(index===3){
                    this.c_content=this.c_content3;
                }else{
                    this.c_content=this.c_content0;
                }
            },
            mEnter(index){
                this.m_match=index;
                if(index==0){
                    this.m_content=this.m_content1;
                    this.match_type=this.match_kpl;
                    this.match_img='kpl';
                }else if(index===1){
                    this.m_content=this.c_content0;
                    this.match_type=this.match_kcc;
                    this.match_img='kcc';
                }else if(index===2){
                    this.m_content=this.c_content1;
                    this.match_type=this.match_kpkpl;
                    this.match_img='kpkpl';
                }else if(index===3){
                    this.m_content=this.c_content2;
                    this.match_type=this.match_koc;
                    this.match_img='koc';
                }else if(index===4){
                    this.m_content=this.c_content3;
                    this.match_type=this.match_gxs;
                    this.match_img='gxs';
                }else if(index===5){
                    this.m_content=this.m_content1;
                    this.match_type=this.match_tga;
                    this.match_img='tga';
                }else if(index===6){
                    this.m_content=this.c_content0;
                    this.match_type=this.match_wgi;
                    this.match_img='wgi';
                }
            }
        },
        mounted() {
            this.m_content=this.m_content1;
            this.match_type=this.match_kpl;
        }

    }
</script>

<style scoped>
.cc-enter-active{
  transition: all .5s ease;
}
.cc-enter, .cc-leave-to
{
  opacity: 0;
}
</style>
