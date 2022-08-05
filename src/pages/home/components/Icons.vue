<template>
  <div class="icons-wrapper">
      <swiper :options="iconsSwiperOptions" ref="mySwiper">
        <!-- slides -->
        <swiper-slide v-for="(page, idx) in pagesList" :key="idx">
          <div class="icon-box" v-for="item in page" :key="item.id">
            <div class="icon-img-box">
              <img  class="icon-img" :src='item.imgUrl' />
            </div>
            <p class="icon-desc">{{ item.desc }}</p>
          </div>
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
import icon1 from '@/assets/image/icon1.svg'
import icon2 from '@/assets/image/icon2.svg'
import icon3 from '@/assets/image/icon3.svg'
import icon4 from '@/assets/image/icon4.svg'
import icon5 from '@/assets/image/icon5.svg'
import icon6 from '@/assets/image/icon6.svg'
import icon7 from '@/assets/image/icon7.svg'
import icon8 from '@/assets/image/icon8.svg'
import icon9 from '@/assets/image/icon9.svg'
import icon10 from '@/assets/image/icon10.svg'
import icon11 from '@/assets/image/icon11.svg'
import icon12 from '@/assets/image/icon12.svg'
export default {
  name: 'HomeIcons',
  data () {
    return {
      iconsSwiperOptions: {
        loop: true,
        autoplay: 0
      },
      iconsList: [
        {
          id: '001',
          imgUrl: icon1,
          desc: '景点门票'
        }, {
          id: '002',
          imgUrl: icon2,
          desc: '一日游'
        }, {
          id: '003',
          imgUrl: icon3,
          desc: '长沙必游'
        }, {
          id: '004',
          imgUrl: icon4,
          desc: '踏青赏花'
        }, {
          id: '005',
          imgUrl: icon5,
          desc: '游乐场'
        }, {
          id: '006',
          imgUrl: icon6,
          desc: '动植物园'
        }, {
          id: '007',
          imgUrl: icon7,
          desc: '自然风光'
        }, {
          id: '008',
          imgUrl: icon8,
          desc: '湘西凤凰'
        }, {
          id: '009',
          imgUrl: icon9,
          desc: '橘子洲'
        }, {
          id: '010',
          imgUrl: icon10,
          desc: '玻璃桥'
        }, {
          id: '011',
          imgUrl: icon11,
          desc: '光谷'
        }, {
          id: '012',
          imgUrl: icon12,
          desc: '庐山'
        }
      ]
    }
  },
  computed: {
    pagesList () {
      const pages = []
      this.iconsList.forEach((item, idx) => {
        let page = Math.floor((idx / 8))
        if (!pages[page]) {
          pages[page] = []
        }
        pages[page].push(item)
      })
      return pages
    }
  }
}

</script>

<style lang="stylus" scoped>
@import "~styles/variables.styl"
@import "~styles/mixins.styl"
.icons-wrapper {
  width: 100%;
  height: 0;
  padding-bottom: 50%;
  overflow: hidden;
  margin: .2rem 0;
}
.icons-wrapper .icon-box {
  float: left;
  width: 25%;
  height: 0;
  padding-bottom: 25%;
  position: relative;
}

.icons-wrapper .icon-box .icon-img-box {
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: .64rem;
}
.icons-wrapper .icon-box .icon-img-box .icon-img {
  height: 100%;
  display: block;
  margin: 0 auto;
}
.icons-wrapper .icon-box .icon-desc {
  color: $darkTextColor;
  position: absolute;
  bottom: 0;
  right: 0;
  left: 0;
  height: .44rem;
  line-height: .44rem;
  text-align: center;
  ellipsis()
}
</style>
