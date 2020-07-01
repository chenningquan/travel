<template>
  <swiper :options="swiperOption" class="icons">
    <swiper-slide class="icon-slide" v-for="(page, index) of pages" :key="index">
      <div class="icon" v-for="item of page" :key="item.id">
        <img :src="item.imgUrl" class="icon-img">
        <p class="icon-desc">{{ item.desc }}</p>
      </div>
    </swiper-slide>
  </swiper>
</template>

<script>
  export default {
    name: "HomeIconList",
    data() {
      return {
        iconList: [{
          id: '0001',
          imgUrl: 'http://img4.imgtn.bdimg.com/it/u=3117526464,609455560&fm=26&gp=0.jpg',
          desc: '景点推荐1'
        },{
          id: '0002',
          imgUrl: 'http://img4.imgtn.bdimg.com/it/u=3117526464,609455560&fm=26&gp=0.jpg',
          desc: '景点推荐2'
        },{
          id: '0003',
          imgUrl: 'http://img4.imgtn.bdimg.com/it/u=3117526464,609455560&fm=26&gp=0.jpg',
          desc: '景点推荐3'
        },{
          id: '0004',
          imgUrl: 'http://img4.imgtn.bdimg.com/it/u=3117526464,609455560&fm=26&gp=0.jpg',
          desc: '景点推荐4'
        },{
          id: '0005',
          imgUrl: 'http://img4.imgtn.bdimg.com/it/u=3117526464,609455560&fm=26&gp=0.jpg',
          desc: '景点推荐5'
        },{
          id: '0006',
          imgUrl: 'http://img4.imgtn.bdimg.com/it/u=3117526464,609455560&fm=26&gp=0.jpg',
          desc: '景点推荐6'
        },{
          id: '0007',
          imgUrl: 'http://img4.imgtn.bdimg.com/it/u=3117526464,609455560&fm=26&gp=0.jpg',
          desc: '景点推荐7'
        },{
          id: '0008',
          imgUrl: 'http://img4.imgtn.bdimg.com/it/u=3117526464,609455560&fm=26&gp=0.jpg',
          desc: '景点推荐8'
        },{
          id: '0009',
          imgUrl: 'http://img4.imgtn.bdimg.com/it/u=3117526464,609455560&fm=26&gp=0.jpg',
          desc: '景点推荐9'
        }],
        swiperOption: {

        }
      }
    },
    computed: {
      pages() {
        const pages = []
        this.iconList.forEach((item, index) => {
          const page = Math.floor(index / 8)
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
  .icons >>> .icon-slide
    width 100%
    height 0
    padding-bottom 50%
  .icons
    .icon
      overflow hidden
      width 25%
      height 0
      padding-bottom 25%
      float left
      .icon-img
        padding-top .24rem
        width 1rem
        height 1rem
        display: block
        margin: 0 auto
      .icon-desc
        text-align center
</style>
