<template>
  <div id="app-root">
    <header class="header">
      <h1>This is my first VueJs project</h1>
    </header>

    <section class="categories-wrap">
      <div class="categories">
        <CategoryCard
          v-for="(c, idx) in categories"
          :key="idx"
          :image-src="c.img"
          :title="c.title"
          :item-count="c.count"
          :bg-color="c.bg"
        />
      </div>
    </section>

    <section class="banners">
      <BannerCard
        v-for="(b, i) in banners"
        :key="i"
        :image-src="b.img"
        :title="b.title"
        :bg="b.bg"
        :btn-color="b.btnColor"
      />
    </section>
  </div>
</template>

<script>
import CategoryCard from './components/CategoryCard.vue'
import BannerCard from './components/Banner.vue'

// if you exported images from src/assets/img/index.js
import {
  burgerImage,
  peachImage,
  appleImage,
  blackPlumImage,
  cakeAndmilkImage,
  headPhoneImage,
  kiwiImage,
  orangeImage,
  snackImage,
  vegetableImage,
  onionImage,
  vegetablesImage,
  milkImage,
} from '@/assets'

export default {
  name: 'App',
  components: { CategoryCard, BannerCard },
  data() {
    return {
      categories: [
        { title: 'Cake & Milk', count: 14, img: burgerImage, bg: '#F2FCE4' },
        { title: 'Peach', count: 17, img: peachImage, bg: '#FFFCEB' },
        { title: 'Organic Kiwi', count: 21, img: kiwiImage, bg: '#ECFFEC' },
        { title: 'Red Apple', count: 68, img: appleImage, bg: '#FEEFEA' },
        { title: 'Snack', count: 34, img: snackImage, bg: '#FFF3EB' },
        { title: 'Black Plum', count: 25, img: blackPlumImage, bg: '#FFF3FF' },
        { title: 'Vegetables', count: 65, img: vegetableImage, bg: '#F2FCE4' },
        { title: 'Headphone', count: 33, img: headPhoneImage, bg: '#FFFCEB' },
        { title: 'Cake & Milk', count: 54, img: cakeAndmilkImage, bg: '#F2FCE4' },
        { title: 'Orange', count: 63, img: orangeImage, bg: '#FFF3FF' },
      ],
      banners: [
        {
          title: 'Everyday Fresh & Clean with Our Products',
          img: onionImage,
          bg: '#F0E8D5',
          btnColor: '#3BB77E',
        },
        {
          title: 'Make your Breakfast Healthy and Easy',
          img: milkImage,
          bg: '#F3E8E8',
          btnColor: '#3BB77E',
        },
        {
          title: 'The best Organic Products Online',
          img: vegetablesImage,
          bg: '#E7EAF3',
          btnColor: '#FDC040',
        },
      ],
    }
  },
}
</script>

<style>
/* simple styles — adjust or replace with your CSS file */
#app-root {
  padding: 24px;
  font-family: Arial, Helvetica, sans-serif;
}
.header h1 {
  font-size: 22px;
  margin-bottom: 18px;
}
.categories {
  display: flex;
  gap: 12px;
  overflow-x: auto;
  padding-bottom: 10px;
}
.banners {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 14px;
  margin-top: 18px;
}
@media (max-width: 900px) {
  .banners {
    grid-template-columns: 1fr;
  }
}
</style>
