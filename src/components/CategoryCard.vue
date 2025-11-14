<template>
  <div class="cat-card" :style="{ background: bgColor }">
    <div class="thumb"><img :src="imageSrc" alt="" /></div>
    <div class="meta">
      <div class="title">{{ title }}</div>
      <div class="count">{{ itemCount }} items</div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'CategoryCard',
  props: {
    imageSrc: String,
    title: String,
    itemCount: Number,
    bgColor: String,
  },
}
</script>

<style scoped>
.cat-card {
  width: 140px;
  padding: 12px;
  border-radius: 10px;
  text-align: center;
  box-shadow: 0 6px 14px rgba(0, 0, 0, 0.06);
}
.thumb img {
  width: 64px;
  height: 64px;
  object-fit: contain;
}
.title {
  font-weight: 600;
  margin-top: 6px;
}
.count {
  font-size: 12px;
  color: #666;
}
</style>
