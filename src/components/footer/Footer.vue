<template>
  <section id='foot_guide'>
    <svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" style="position:absolute;width:0;height:0">
      <defs>
        <symbol xmlns:xlink="http://www.w3.org/1999/xlink" viewBox="0 0 40 40" id="home">
          <defs>
            <path id="discover-regular.8ef537f_a" d="M20 40c11.046 0 20-8.954 20-20S31.046 0 20 0 0 8.954 0 20s8.954 20 20 20z"></path>
            <mask id="discover-regular.8ef537f_b" width="40" height="40" x="0" y="0" fill="#fff">
              <use xlink:href="#discover-regular.8ef537f_a"></use>
            </mask>
          </defs>
          <g fill="none" fill-rule="evenodd">
            <use stroke="#666" stroke-width="4" mask="url(#discover-regular.8ef537f_b)" xlink:href="#discover-regular.8ef537f_a"></use>
            <path stroke="#666" stroke-width="2" d="M12.79 28.126c-1.515.68-2.169.016-1.462-1.484l3.905-8.284c.47-.999 1.665-2.198 2.66-2.675l8.484-4.064c1.497-.717 2.153-.08 1.46 1.435l-3.953 8.64c-.46 1.006-1.647 2.186-2.655 2.64l-8.44 3.792z"></path>
            <path fill="#666" d="M15.693 24.636c-.692.276-1.02-.06-.747-.746l2.21-4.946c.225-.505.721-.602 1.122-.202l2.563 2.563c.394.394.31.893-.203 1.122l-4.945 2.209z"></path>
          </g>
        </symbol>

        <symbol xmlns:xlink="http://www.w3.org/1999/xlink" viewBox="0 0 40 40" id="homeActive">
          <defs>
            <path id="discover-regular.8ef537f_a" d="M20 40c11.046 0 20-8.954 20-20S31.046 0 20 0 0 8.954 0 20s8.954 20 20 20z"></path>
            <mask id="discover-regular.8ef537f_b" width="40" height="40" x="0" y="0" fill="#fff">
              <use xlink:href="#discover-regular.8ef537f_a"></use>
            </mask>
          </defs>
          <g fill="none" fill-rule="evenodd">
            <use stroke="#3190e8" stroke-width="4" mask="url(#discover-regular.8ef537f_b)" xlink:href="#discover-regular.8ef537f_a"></use>
            <path stroke="#3190e8" stroke-width="2" d="M12.79 28.126c-1.515.68-2.169.016-1.462-1.484l3.905-8.284c.47-.999 1.665-2.198 2.66-2.675l8.484-4.064c1.497-.717 2.153-.08 1.46 1.435l-3.953 8.64c-.46 1.006-1.647 2.186-2.655 2.64l-8.44 3.792z"></path>
            <path fill="#3190e8" d="M15.693 24.636c-.692.276-1.02-.06-.747-.746l2.21-4.946c.225-.505.721-.602 1.122-.202l2.563 2.563c.394.394.31.893-.203 1.122l-4.945 2.209z"></path>
          </g>
        </symbol>

        <symbol xmlns:xlink="http://www.w3.org/1999/xlink" viewBox="0 0 38 38" id="order">
          <defs>
            <rect id="order-regular.41c17f8_a" width="38" height="38" rx="2"></rect>
            <mask id="order-regular.41c17f8_b" width="38" height="38" x="0" y="0" fill="#fff">
              <use xlink:href="#order-regular.41c17f8_a"></use>
            </mask>
          </defs>
          <g fill="none" fill-rule="evenodd">
            <use stroke="#666" stroke-width="4" mask="url(#order-regular.41c17f8_b)" xlink:href="#order-regular.41c17f8_a"></use>
            <rect width="24" height="2" x="7" y="8" fill="#666" rx="1"></rect>
            <rect width="20" height="2" x="7" y="17" fill="#666" rx="1"></rect>
            <rect width="8" height="2" x="7" y="26" fill="#666" rx="1"></rect>
          </g>
        </symbol>

        <symbol viewBox="0 0 38 38" id="orderActive">
          <defs>
            <linearGradient id="order.070ae2a_a" x1="50%" x2="50%" y1="100%" y2="0%">
              <stop offset="0%" stop-color="#2BAEFF"></stop>
              <stop offset="100%" stop-color="#0095FF"></stop>
            </linearGradient>
          </defs>
          <g fill="none" fill-rule="evenodd">
            <rect width="38" height="38" fill="url(#order.070ae2a_a)" rx="2"></rect>
            <rect width="24" height="2" x="7" y="8" fill="#FFF" rx="1"></rect>
            <rect width="20" height="2" x="7" y="17" fill="#FFF" rx="1"></rect>
            <rect width="8" height="2" x="7" y="26" fill="#FFF" rx="1"></rect>
          </g>
        </symbol>
      </defs>
    </svg>
    <section @click="gotoAddress('/home')" class="guide_item">
      <svg class="icon_style">
        <use xmlns:xlink="http://www.w3.org/1999/xlink" :xlink:href="$route.path.indexOf('home') !== -1? '#homeActive' : '#home'"></use>
      </svg>
      <span>首页</span>
    </section>
    <section @click="gotoAddress('/order')" class="guide_item">
      <svg class="icon_style">
        <use xmlns:xlink="http://www.w3.org/1999/xlink" :xlink:href="$route.path.indexOf('order') !== -1? '#orderActive' : '#order'"></use>
      </svg>
      <span>我的订单</span>
    </section>
  </section>
</template>

<script>
import {mapState} from 'vuex'
export default {
  data () {
    return {}
  },
  created () {},
  mounted () {},
  computed: {
    ...mapState([
      'geohash'
    ])
  },
  methods: {
    gotoAddress (path) {
      this.$router.push(path)
    }
  }
}
</script>

<style lang="scss" scoped>
  @import '@/styles/mixin.scss';

  #foot_guide {
    background-color: #fff;
    position: fixed;
    z-index: 100;
    left: 0;
    right: 0;
    bottom: 0;
    @include wh(100%, 1.95rem);
    display: flex;
    box-shadow: 0 -0.026667rem 0.053333rem rgba(0, 0, 0, .1);
  }

  .guide_item {
    flex: 1;
    display: flex;
    text-align: center;
    flex-direction: column;
    align-items: center;

    .icon_style {
      @include wh(.8rem, .8rem);
      margin-top: .3rem;
      fill: #ccc;
    }

    span {
      @include sc(.45rem, #666);
    }
  }

</style>
