<template>
  <div class="box">
    <div class="swiper-container">
      <div class="swiper-wrapper">
        <div class="swiper-slide"><img src="https://gimg2.baidu.com/image_search/src=http%3A%2F%2Fdingyue.ws.126.net%2F2020%2F0515%2F465567a6j00qadpfz001cc000hs00b4c.jpg&refer=http%3A%2F%2Fdingyue.ws.126.net&app=2002&size=f9999,10000&q=a80&n=0&g=0n&fmt=auto?sec=1662275243&t=34f6fe8517baca8d461577129887494d" alt=""></div>
        <div class="swiper-slide"><img src="https://img1.baidu.com/it/u=724179003,4096104503&fm=253&fmt=auto&app=138&f=JPEG?w=750&h=500" alt=""></div>
        <div class="swiper-slide"><img src="https://gimg2.baidu.com/image_search/src=http%3A%2F%2Fimg.jj20.com%2Fup%2Fallimg%2Ftp05%2F19100220062L3N-0-lp.jpg&refer=http%3A%2F%2Fimg.jj20.com&app=2002&size=f9999,10000&q=a80&n=0&g=0n&fmt=auto?sec=1662275243&t=1dae8305d25e80a2fb33d1ff6cf639f3" alt=""></div>
      </div>
      <div class="swiper-pagination"></div>
    </div>
  </div>
</template>
<script>
import Swiper from "swiper";
import "swiper/dist/css/swiper.min.css";
export default {
  mounted() {
    new Swiper(".swiper-container", {
      //指示点 
      pagination: ".swiper-pagination",
      //方向:垂直
      direction: "vertical",
      //循环
      loop:true,
      //点击指示点滑动
      paginationClickable:true,
      //渐变效果 slide的切换效果，默认为"slide"（位移切换），可设置为"fade"（淡入）"cube"（方块）"coverflow"（3d流）"flip"（3d翻转）。 
      effect:'fade',
    });
  },
};
</script>
<style>
.swiper-container {
  width: 1000px;
  height: 500px;
  border: 1px solid;
  margin-bottom: 10px;
  cursor: pointer;
}
.swiper-slide {
  text-align: center;
  font-size: 18px;
  background: #fff;
  height: 100%;
  width: 100%;

  /* Center slide text vertically */
  display: -webkit-box;
  display: -ms-flexbox;
  display: -webkit-flex;
  display: flex;
  -webkit-box-pack: center;
  -ms-flex-pack: center;
  -webkit-justify-content: center;
  justify-content: center;
  -webkit-box-align: center;
  -ms-flex-align: center;
  -webkit-align-items: center;
  align-items: center;
}
.swiper-slide img{
    width: 100%;
}
.swiper-pagination-bullet{
    width: 15px;
    height: 15px;
    background-color: #fff;
    opacity: .8;
}
.swiper-pagination-bullet-active{
    background-color:#ffe76f;
    opacity: 1;
}
</style>