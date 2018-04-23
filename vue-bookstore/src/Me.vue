<template>
<div>
    <div class="desc-wrap">
    <div class="me">
        <img src="./assets/images/me.png" alt="">
    </div>
    <div class="desc">
        Huhui-coder
    </div>
     <div class="user">
       用户名： Huhui-coder
    </div>
    <div class="userdesc">
        尊贵的高级会员，欢迎来到图书商城
    </div>
    <div class="option">
         <button class="one">
             甜蜜生活
         </button>
          <button class="two">
             IT
         </button>
         <button class="three">
             魅力男生
         </button>
          <button class="four">
             养生之道
         </button>
    </div>
   </div>
   <div class="dian">
     最新咨询：你爱的全都有
   </div>
   <div class="contant">
     <div class="contant-desc">
         <span>
             <img src="./assets/images/apparel.svg" alt="">
              <span class="span-desc">服装</span>
         </span>
         <span>
             <img src="./assets/images/bags.svg" alt="">
              <span class="span-desc">包包</span>
         </span>
         <span>
             <img src="./assets/images/cart.svg" alt="">
              <span class="span-desc">购物车</span>
         </span>
         <span class="huazhuang">
             <img src="./assets/images/category.svg" alt="">
              <span class="span-desc">化妆</span>
         </span>
        <span class="shoucang"> 
             <img src="./assets/images/favorites-filling.svg" alt="">
              <span class="span-desc">收藏</span>
         </span>
         <span class="home">
             <img src="./assets/images/home.svg" alt="">
              <span class="span-desc">  &nbsp;家</span>
         </span>
     </div>
   </div>
   <div class="main">

   </div>
    </div>
</template>
<style>
.desc-wrap{
    width: 90%;
    background-color:;
    position: relative;
    height: 200px;  
    margin: 5px auto;
    border-radius: 8px 8px 0 0;
    background-color: rgba(255,0,0,.6)
}
    .me img{
        height: 100px;
        width: 100px;
        border-radius: 50%;
        position: absolute;
        top: 10%;
        left: 5%;
    }
    .desc{
        position: absolute;
        top: 10%;
        left: 40%;
        color: papayawhip;
        
    }
    .user{
        position: absolute;
        top: 25%;
        left: 40%;
        color:rgba(248, 241, 241,.6);
    }
    .userdesc{
        position: absolute;
        top: 40%;
        left: 40%;
         color:rgba(248, 241, 241,.8);
    }
    .option{
        position: absolute;
        width: 100%;
        height: 60px;
        bottom: 0;
        background-color: rgba(248, 241, 241,.6);
    }
    .option >button{
        margin:  15px 5px;
    border: none;
    border-radius: 30px;
    font-size: 16px;
    }
     .option > .one{
         background-color:rgba(248, 241, 241,.6);
    }
      .option > .two{
         background-color:rgba(185, 154, 154, 0.6);
    }
      .option > .three{
         background-color:rgba(109, 80, 80, 0.6);
    }
      .option > .four{
         background-color:rgba(107, 64, 64, 0.6);
    }
    .dian{
        margin: 10px;
        width: 90%;
        height: 17px;
        background-color: rgba(248, 241, 241,.8);
        font-size: 17px;
        padding: 10px;
        line-height: 17px;

    }
    .contant{
        margin: 10px auto;
        width: 90%;
        height: 160px;
        background-color: rgba(214, 203, 203, 0.3);
        font-size: 17px;
        padding: 10px;
        line-height: 17px;
        border-radius: 18px;
    }
    .contant-desc >span{
        margin: 15px;
        padding: 15px;
        position: relative;
      
}
    .content-desc{
        position: relative;   
    }
    .span-desc{
        position: absolute;
        top: 40px;
        left: 15px;
    }
     .huazhuang{
        position: absolute;
        top: 50px;
    }
    .shoucang{
        position: absolute;
        top: 50px;
    }
    .home{
        position: absolute;
        top: 50px;
    }
  
    </style>
<script type="text/ecmascript-6">
    export default{}
</script>