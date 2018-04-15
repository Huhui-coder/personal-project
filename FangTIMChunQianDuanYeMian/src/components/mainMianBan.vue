<template>
  <div>
    <div class="mianMianBan" >
      <div class="top-ban clearfix">
        <div class="sm-touxiang fl" @click="toplist=2,toplist1=2" :class="{ 'visible':toplist === 1,'sm-touxiang-border':toplist ===2}"></div>
        <div class="touxiang-list"  @click="toplist=1,toplist1=1" :class="{ 'hidden':toplist1 === 1,'visible':toplist1=== 2}">
          <div class="touxiang-name">
            <p>Hit</p>
            <span>请编辑你的个性签名</span>
          </div>
          <ul class="fa-ul">
            <li><i class="fa fa-cloud fa-fw"></i>微云</li>
            <li><i class="fa fa-calendar-check-o fa-fw"></i>日程</li>
            <li><i class="fa fa-star-o fa-fw"></i>收藏</li>
            <li><i class="fa fa-envelope-open-o fa-fw"></i>邮箱</li>
            <li><i class="fa fa-volume-down fa-fw"></i>消息管理器</li>
            <li class="fuli"><i class="fa fa-gift fa-fw"></i>福利</li>
            <li><b></b>在线</li>
            <li><b></b>切换账号</li>
            <router-link to="/"><li><b></b>退出账号</li></router-link>
          </ul>
        </div>
        <div class="found">
          <i class="fa fa-search"></i>
        </div>
        <div class="test-box clearfix">
          <router-link to="/Message">
            <div class="test-tab fl" @click="message = 1,friends = 2,onLineWord =2" :class="{ 'test-tab':message === 2,'active':message === 1 }">
              <i class="test fa fa-wechat op"></i><br>
              <span class="sanjiao op">&#9650</span>
            </div>
          </router-link>
          <router-link to="/Friends">
            <div class="test-tab fl" @click="message = 2,friends = 1,onLineWord =2" :class="{ 'test-tab':friends === 2,'active':friends === 1 }">
              <i class="test fa fa-address-card-o op"></i><br>
              <span class="sanjiao op">&#9650</span>
            </div>
          </router-link>
          <router-link to="/onLineWord">
            <div class="test-tab fl" @click="message = 2,friends = 2,onLineWord =1" :class="{ 'test-tab':onLineWord === 2,'active':onLineWord === 1 }" >
              <i class="test fa fa-file-o op"></i><br>
              <span class="sanjiao op">&#9650</span>
            </div>
          </router-link>
        </div>
        <div class="gongneng fl">
          <i class="fa fa-navicon"></i>
          <i class="fa fa-minus"></i>
          <i class="fa fa-square-o"></i>
          <i class="fa fa-times hover-red"></i>
        </div>
      </div>
    <router-view></router-view>
    </div>
  </div>
</template>

<script>
import Firends from './Friends.vue'
import Message from './Message.vue'
import onLineWord from './onLineWord.vue'
  export default {
  data(){
    return{
      message:1,
      friends:2,
      onLineWord:2,
      toplist:1,
      toplist1:1
    }
  },
    components:{
      Firends,
      Message,
      onLineWord,
    }
  }
</script>

<style scoped>
  .mianMianBan{
    margin-top: 5%;
    margin-left: auto;
    margin-right: auto;
    width: 800px;
  }
  .top-ban{
    height: 55px;
    background-image: url("../assets/banenr-logo.png");
    border-top-right-radius: 7px;
    border-top-left-radius: 7px;
    width: 800px;
    box-shadow: 0 -3px 9px #898989;
    position: relative;
    top: 4px;
  }
  .sm-touxiang{
    width: 40px;
    height: 40px;
    border-radius: 40px;
    background-image: url("../assets/touxiang.jpg");
    background-size: cover;
    position: relative;
    border: 1px solid #2E9BE9;
    top: 7px;
    left: 7px;
  }
  .touxiang-list{
    position: relative;
    background-color: #FFFFFF;
    z-index: 2;
    width: 182px;
    top: 55px;
    float: left;
    right: 41px;
  }
  .touxiang-list ul i{
    margin-right: 5px;
    color: #A0A0A1;
  }
  .touxiang-list ul b{
    margin-left: 25px;
  }
  .touxiang-list ul li{
    cursor: pointer;
    line-height: 35px;
    padding-left: 10px;
    margin-left: -11px;
    font-size: 14px;
  }
  .touxiang-list ul li:hover{
    background-color: #EBECEE;
  }
  .sm-touxiang:hover{
    border: 1px solid #D4EBFB ;
  }
  .sm-touxiang-border{
    border: 1px solid #D4EBFB ;
  }
  .touxiang-name{
    height: 65px;
    border-bottom: 1px solid #F5F5F5;
  }
  .touxiang-name p{
    padding: 10px 0 0 8px;
  }
  .touxiang-name span{
    padding-left: 8px;
    color: #767676;
    font-size: 12px;
  }
  .touxiang-list ul{
    padding-left: 10px;
    margin-left: 0;
  }
  .fuli{
    padding: 7px 0 7px 0;
    border-bottom: 1px solid #F5F5F5;
    border-top: 1px solid #F5F5F5;
  }
  .found{
    width: 95px;
    height: 22px;
    border-radius: 22px;
    border: 1px solid #FFFFFF;
    color: #FFFFFF;
    opacity: 0.4;
    position: relative;
    left: 80px;
    top: 15px;
  }
  .found i{
    position: absolute;
    left: 8px;
    top: 3px;

  }
  .found:hover{
    color: #FFFFFF;
    opacity: 1.0;
  }
  .test-box{
    margin-left: 10px;
    margin-top: -10px;
  }
  .test-tab{
    margin-right: 35px;
  }
  .test-tab .sanjiao{
    position: relative;
    color: #FFFFFF;
    top:0;
    left: 5px;
    opacity: 0;
  }
  .test-tab i{
    color: #FFFFFF;
    font-size: 25px;
    opacity: 0.7;
  }
  .test-box .active .op,.test-box .active .op{opacity: 1.0}
  .test-box .test:hover{opacity: 1.0}

  .gongneng{
    position: relative;
    left: 480px;
    top: -6px;
  }
  .gongneng i{
    color: #FFFFFF;
    opacity: 0.6;
    margin-right: 5px;
  }
  .gongneng i:hover{
    opacity: 1.0;
  }
  .hover-red{
    padding: 3px;
  }
  .hover-red:hover{
    background-color: red;
    padding: 3px;
  }
</style>
