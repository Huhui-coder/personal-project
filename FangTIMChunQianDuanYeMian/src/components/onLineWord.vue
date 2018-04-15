<template>
  <div>
    <div class="onlineword">
      <div class="olw-top clearfix">
        <p class="fl">云文件</p>
        <div class="olw-top-i fr">
          <i class="fa fa-search"></i>
          <i class="fa fa-refresh"></i>
          <span>新建 <i class="fa fa-caret-down"></i></span>
        </div>
      </div>
      <div class="olw-welcome"  :class="{ 'dn':close === 1}">
        <h3>欢迎使用云文件</h3>
        <ul>
          <li>● 为你提供10G免费的安全存储空间；自动保存手法文件，长期有效。</li>
          <li>● 支持任意设备，随时随地编辑Word和Excel，可邀请他人同时编辑。</li>
        </ul>
        <p @click="close = 1">我知道了</p>
        <div class="olw-colorbox-1"></div>
        <div class="olw-colorbox-2"></div>
        <div class="olw-colorbox-3"></div>
      </div>
      <div class="olw-wenjian clearfix">
        <div class="file-fenlei clearfix">
          <div class="file-box fl" @click="box1 = 1,box2=2,box3=2,box4=2" :class="{ 'file-box-click':box1 === 1, 'file-box-none':box1 === 2}">
            <div class="file-img">
              <img src="../assets/box-file.png" alt="">
              <img src="../assets/box-file.png" alt="">
              <img src="../assets/box-file.png" alt="">
              <img src="../assets/box-file.png" alt="">
            </div>
            <p>全部文件</p>
            <span>4项</span>
          </div>
          <div class="file-box fl" @click="box1 = 2,box2=1,box3=2,box4=2" :class="{ 'file-box-click':box2 === 1, 'file-box-none':box2 === 2}">
            <div class="file-img">
              <img src="../assets/box-file.png" alt="">
              <img src="../assets/box-file.png" alt="">
              <img src="../assets/box-file.png" alt="">
            </div>
            <p>在线文档</p>
            <span>3项</span>
          </div>
          <div class="file-box fl" @click="box1 = 2,box2=2,box3=1,box4=2" :class="{ 'file-box-click':box3 === 1, 'file-box-none':box3 === 2}">
            <div class="file-img">
              <img src="../assets/box-file.png" alt="">
              <img src="../assets/box-file.png" alt="">
            </div>
            <p>收发文件</p>
            <span>2项</span>
          </div>
          <div class="file-box fl" @click="box1 = 2,box2=2,box3=2,box4=1" :class="{ 'file-box-click':box4 === 1, 'file-box-none':box4 === 2}">
            <div class="file-img">
              <img src="../assets/box-file.png" alt="">
            </div>
            <p>未分类文件</p>
            <span>1项</span>
          </div>
        </div>
      </div>
      <p class="olw-bottom">TIM云文件：剩余9.93GB，共10GB。<span class="font-c-b">了解更多 ></span></p>
    </div>
  </div>
</template>

<script>
export default {
  data (){
    return{
      box1:2,
      box2:2,
      box3:2,
      box4:2,
      close:2
    }
  }
}
</script>

<style>
  .onlineword{
    width: 800px;
    height: 540px;
    overflow: hidden;
    box-shadow: 0 3px 9px #898989;
    position: relative;
    top:-4px;
  }
  .olw-top{
    width: 100%;
    border-bottom: 1px solid #EAEAEA;
  }
  .olw-top p{
    line-height: 44px;
    font-size: 14px;
    margin-left: 25px;
  }
  .dn{
    display: none;
  }
  .olw-top-i{
    line-height: 44px;
    position: relative;
    right: 20px;
  }
  .olw-top-i i{
     color: #9F9F9F;
     font-size: 20px;
     margin-right: 7px;
     padding: 5px;
    cursor: pointer;
   }
  .olw-top-i i:hover{
    background-color: #EBECEE;
  }
  .olw-top-i span{
    color: #FFFFFF;
    background-color: #0188FB;
    border: none;
    padding: 4px 8px;
    border-radius: 3px;
    line-height: 31px;
    cursor: pointer;
  }
  .olw-top-i span:hover{
    background-color:#289DFF;
  }
  .olw-top-i span i{
    font-size: 10px;
    padding: 4px;
    margin-right: 0;
    color: #FFFFFF;
  }
  .olw-top-i span i:hover{
    background-color: transparent;
  }
  .olw-welcome{
    border-bottom: 1px solid #EAEAEA;
    text-align: center;
  }
  .olw-welcome h3{
    margin-top: 20px;
    font-size: 20px;
    line-height: 30px;
    font-weight: 500;
  }
  .olw-welcome ul li{
    color: #777777;
    font-size: 14px;
  }
  .olw-welcome p{
    line-height: 46px;
    color: #008EFA;
    font-size: 13px;
    cursor: pointer;
  }
  .olw-colorbox-1{
    width: 27px;
    height: 27px;
    position: absolute;
    background-color: #3E58C9;
    top: 65px;
  }
  .olw-colorbox-2{
    width: 35px;
    height: 32px;
    background-color: #0086F1;
    position: absolute;
    right: 0;
    top: 120px;
  }
  .olw-colorbox-3{
    width: 27px;
    height: 19px;
    background-color: #3E58C9;
    opacity: 0.9;
    position: absolute;
    right: 23px;
    top: 143px;
  }
  .file-fenlei{
    margin-top: 12px;
    margin-left: 16px;
  }
  .file-box{
    padding: 9px;
    border: 1px solid transparent;
    margin-right: 5px;
    cursor: pointer;
  }
  .file-box-none{}
  .file-box-click{
    border: 1px solid #CED8EA;
    background-color: #F9FBFE;
  }
  .file-box:hover{
    border: 1px solid #CED8EA;
    background-color: #F9FBFE;
  }
  .file-img{
    width: 122px;
    height: 106px;
    border-radius: 3px;
    background-color: #E6E9ED;
  }
  .file-img img{
    margin: 4px 0px 0 4px;
  }
  .file-box p{
    font-size: 14px;
    margin-top: 6px;
  }
  .file-box span{
    font-size: 12px;
    color: #767676;
    position: relative;
    top: -4px;
  }
  .olw-bottom{
    left: 34%;
    position: absolute;
    bottom: 0;
    font-size: 12px;
    line-height: 35px;
    color: #767676;
  }
  .olw-bottom span{
    color: #008EFA;
    cursor: pointer;
  }
</style>
