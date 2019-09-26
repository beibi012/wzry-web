<template>
<div id="ost">
  <a href=""><img class="ost_img3" src="../../images/game-logo.png"/></a>
  <a href=""><img @mouseenter="img1Enter"   class="ost_img2" src="../../images/ost2.jpg" /></a>
  <a  href=""><span class="ost_p1">成长守护平台</span></a>
  <a  href=""><span class="ost_p2">腾讯游戏排行</span></a>
  <a href=""><img v-show="ost_img1_see"  @mouseleave="img1Leave"class="ost_img1" src="../../images/ost1.jpg" /></a>
</div>
</template>

<script>
    export default {
        name: "ost",
        data(){
            return{
                ost_img1_see:false
            }
        },
        methods:{
            img1Enter(){
                this.ost_img1_see=true;
            },
            img1Leave(){
                this.ost_img1_see=false;
            }
        }
    }
</script>

<style scoped>

</style>
