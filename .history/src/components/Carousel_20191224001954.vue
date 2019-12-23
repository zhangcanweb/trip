<template>
  <swiper :options="swiperOption" ref="mySwiper">
    <swiper-slide v-for="(item, index) in bannerList" :key="index" class="carousel-slider">
      <a :href="item.url">
        <img :src="item.icon" alt />
      </a>
    </swiper-slide>
    <div class="swiper-pagination" slot="pagination"></div>
  </swiper>
</template>

<script>
export default {
  data () {
    return {
      swiperOption: {
        autoplay: true,
        height: 300
      },
      bannerList: [
        {
          icon:
            'https://www.devio.org/io/flutter_app/img/banner/100h10000000q7ght9352.jpg',
          url:
            'https://gs.ctrip.com/html5/you/travels/1422/3771516.html?from=https%3A%2F%2Fm.ctrip.com%2Fhtml5%2F'
        },
        {
          icon:
            'https://dimg04.c-ctrip.com/images/300h0u000000j05rnD96B_C_500_280.jpg',
          url:
            'https://m.ctrip.com/webapp/vacations/tour/detail?productid=3168213&departcityid=2&salecityid=2&from=https%3A%2F%2Fm.ctrip.com%2Fhtml5%2F'
        },
        {
          icon: 'http://pages.ctrip.com/hotel/201811/jdsc_640es_tab1.jpg',
          url:
            'https://m.ctrip.com/events/jiudianshangchenghuodong.html?disable_webview_cache_key=1'
        },
        {
          icon:
            'https://dimg03.c-ctrip.com/images/fd/tg/g1/M03/7E/19/CghzfVWw6OaACaJXABqNWv6ecpw824_C_500_280_Q90.jpg',
          url:
            'https://m.ctrip.com/webapp/vacations/tour/detail?productid=53720&departcityid=2&salecityid=2&from=https%3A%2F%2Fm.ctrip.com%2Fhtml5%2F'
        }
      ]
    }
  }
}
</script>

<style scoped lang="scss">
@import "@/assets/style/fn.scss";
  .carousel-slider {
    img {
      width: 100%;
      height: 100%;
    }
  }
</style>
