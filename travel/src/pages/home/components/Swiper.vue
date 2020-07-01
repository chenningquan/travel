<template>
  <div class="wrapper">
    <swiper :options="swiperOption" v-if="showSwiper">
      <swiper-slide v-for="item of list" :key="item.id">
        <img class="swiper-img" :src="item.imgUrl" />
      </swiper-slide>
      <div class="swiper-pagination"  slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
  export default {
    name: 'HomeSwiper',
    // props: {
    //   list: Array
    // },
    data () {
      return {
        swiperOption: {
          pagination: {
            el: '.swiper-pagination',
            clickable: true
          },
          loop: true,
          autoplay: {
            delay: 3000,
            disableOnInteraction: false
          }
        },
        list: [{
          id: '001',
          imgUrl: 'https://ss1.bdstatic.com/70cFuXSh_Q1YnxGkpoWK1HF6hhy/it/u=3959588730,3008729223&fm=26&gp=0.jpg'
        },{
          id: '002',
          imgUrl: 'https://ss0.bdstatic.com/70cFuHSh_Q1YnxGkpoWK1HF6hhy/it/u=1512995945,949670399&fm=26&gp=0.jpg'
        },{
          id: '003',
          imgUrl: 'https://ss3.bdstatic.com/70cFv8Sh_Q1YnxGkpoWK1HF6hhy/it/u=348849428,290031991&fm=26&gp=0.jpg'
        }]
      }
    },
    computed: {
      showSwiper () {
        return this.list.length
      }
    }
  }
</script>

<style lang="stylus" scoped>
  .wrapper >>> .swiper-pagination-bullet-active
    background: #fff
  .wrapper
    overflow: hidden
    width: auto
    height: auto
    max-width: 100%
    max-height: 100%
    background: #eee
    .swiper-img
      width: 100%
</style>
