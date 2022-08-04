<!-- The ref attr used to find the swiper instance -->
<template>
  <div class="sw-wrapper">
    <swiper :options="swiperOptions" ref="mySwiper">
    <!-- slides -->
    <swiper-slide v-for="item in swiperList" :key="item.id">
      <img class="swiper-image" :id="item.id" :src="item.imgUrl" />
    </swiper-slide>
    <!-- Optional controls -->
    <div class="swiper-pagination"  slot="pagination"></div>
<!--    <div class="swiper-button-prev" slot="button-prev"></div>-->
<!--    <div class="swiper-button-next" slot="button-next"></div>-->
<!--    <div class="swiper-scrollbar"   slot="scrollbar"></div>-->
  </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeSwiper',
  data () {
    return {
      swiperOptions: {
        pagination: '.swiper-pagination',
        loop: true
      },
      swiperList: [
        {
          id: '001',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1705/66/66e7d0114b541a57a3.img.jpg_600x330_228d4caf.jpg'
        },{
          id: '002',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1503/55/5577ab22b2e205d0.water.jpg_600x330_2a541cbf.jpg'
        },{
          id: '003',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1911/58/58502170165daf88a3.img.jpg_600x330_94e7d9e6.jpg'
        },{
          id: '004',
          imgUrl: 'http://qimgs.qunarzz.com/piao_qsight_provider_piao_qsight_web/01024120008jqlio51320.jpg_600x330_e65bd8fd.jpg'
        },
      ]
    }
  }

}
</script>
<style lang="stylus" scoped>
.sw-wrapper >>> .swiper-pagination-bullet-active {
  background-color: #ffffff;
}
.sw-wrapper {
  overflow: hidden;
  width: 100%;
  height: 2.5rem;
  //padding-bottom: 26.67%;
  background-color: #eee;
}
.sw-wrapper .swiper-container {
  height 100%;
}
.sw-wrapper .swiper-image {
  width: 100%;
  height: 100%;
}
</style>
