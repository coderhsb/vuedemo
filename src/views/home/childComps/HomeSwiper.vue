<template>
  <div>
    <swiper>
      <swiper-item v-for="item in banner" :key="item.title">
        <a :href="item.link">
          <img :src="item.image" alt=""/>
        </a>
      </swiper-item>
    </swiper>
  </div>
</template>
<script>
import { Swiper, SwiperItem } from "@/components/common/swiper/index";
export default {
  name: "HomeSwiper",
  components: {
    Swiper,
    SwiperItem
  },
  props: {
    banner: {
      type: Array,
      default() {
        return [];
      }
    }
  }
};
</script>
<style scoped></style>
