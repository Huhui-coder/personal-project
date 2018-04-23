<template>
    <div>
      <div class="section">
          <div class="book-wrap">
          <span><i>1</i>IT类</span>
          </div>
          <div class="book-list">
              <img src="./assets/images/2.png" alt="">
          </div>
      </div>
       <div class="section">
          <span><i>1</i>科技类</span>
          <div class="book-list">
              <img src="./assets/images/3.png" alt="">
          </div>
      </div>
       <div class="section">
          <span><i>1</i>休闲类</span>
          <div class="book-list">
              <img src="./assets/images/1.png" alt="">
          </div>
      </div>
     </div>
</template>
<style>
    .section{
        width: 100%;
        height: 360px;
    }

    span{
        width: 100%;
        height: 16px;
        font-size: 16px;
        line-height: 16px;
    }
    span i{
        width: 2px;
        height: 100%;
        background-color: firebrick;
    }
    img :hover{
         border: 1px solid red;
    }
</style>
<script type="text/ecmascript-6">
    export default{}
</script>