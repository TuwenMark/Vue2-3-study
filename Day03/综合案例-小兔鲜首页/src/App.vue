<template>
  <div>
    <!-- 快捷链接 -->
    <ShortCut />
    <!-- 顶部导航 -->
    <HeaderNav />
    <!-- 轮播区域 -->
    <Banner />
    <!-- 新鲜好物 -->
    <NewGood />
    <!-- 热门品牌 -->
    <HotBrand />
    <!-- 最新专题 -->
    <NewestTopic />
    <!-- 版权底部 -->
    <Footer />
  </div>
</template>

<script>
import ShortCut from '@/components/ShortCut.vue'
import HeaderNav from '@/components/HeaderNav.vue'
import Banner from '@/components/Banner.vue'
import NewGood from '@/components/NewGood.vue'
import HotBrand from '@/components/HotBrand.vue'
import NewestTopic from '@/components/NewestTopic.vue'
import Footer from '@/components/Footer.vue'

export default {
  components: {
    ShortCut,
    HeaderNav,
    Banner,
    NewGood,
    HotBrand,
    NewestTopic,
    Footer,
  },
}
</script>

<style></style>
