<template>
  <div class="wrapper">
    <swiper ref="mySwiper" :options="swiperOptions">
    <swiper-slide v-for="(item) in swiperList" :key="item.id">
      <img src="item.imgUrl" alt="" class="swiper-img">
    </swiper-slide>
    <div class="swiper-pagination" slot="pagination"></div>
  </swiper>
  </div>
</template>

<script>
export default {
  name: 'carrousel',
  data () {
    return {
      swiperOptions: {
        pagination: {
          el: '.swiper-pagination'
        }
      },
      swiperList: [{
      }]
    }
  },
  computed: {
    swiper () {
      return this.$refs.mySwiper.$swiper
    }
  },
  mounted () {
    console.log('Current Swiper instance object', this.swiper)
    this.swiper.slideTo(3, 1000, false)
  }
}
</script>

<style scoped lang="stylus">
.wrapper >>> .swiper-pagination-bullet-active
    background #fff
.wrapper
  overflow hidden
  width 100%
  height 0
  padding-bottom 31.25%
  background #eee
  .swiper-img
    width 100%
</style>
