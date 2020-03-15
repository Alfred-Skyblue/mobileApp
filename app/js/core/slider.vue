<template>
  <section :class="cname">
    <swiper :options="options" :not-next-tick="options.notNextTick">
      <swiper-slide v-for="item in items" :key="item.href">
        <router-link to="{name:item.href}">
          <img src="" alt="" />
        </router-link>
      </swiper-slide>
      <div class="swiper-pagination" v-if="options.pagination"></div>
    </swiper>
  </section>
</template>

<script>
import { swiper, swiperSlide } from 'vue-awesome-swiper'
export default {
  name: 'slider',
  props: {
    options: {
      type: Object,
      default() {
        return {
          autoplay: true,
          loop: true,
          pagination: {
            el: '.swiper-pagination'
          },
          notNextTick: false
        }
      },
      items: {
        type: Array,
        default() {
          return []
        }
      }
    },
    cname: {
      type: String,
      default() {
        return ''
      }
    }
  },
  components: {
    swiper,
    swiperSlide
  }
}
</script>

<style lang="scss" scoped>
@import '~swiper/dist/css/swiper.css';
</style>
