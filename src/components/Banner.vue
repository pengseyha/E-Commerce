<template>
  <div class="banner" :style="{ background: bg }">
    <div class="left">
      <h3>{{ title }}</h3>
      <button :style="{ background: btnColor }">Shop Now →</button>
    </div>
    <div class="right">
      <img :src="imageSrc" alt="" />
    </div>
  </div>
</template>

<script>
export default {
  name: 'BannerCard',
  props: {
    title: String,
    imageSrc: String,
    bg: String,
    btnColor: String,
  },
}
</script>

<style scoped>
.banner {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 16px;
  border-radius: 12px;
  min-height: 140px;
}

.left h3 {
  margin: 0 0 8px;
  font-size: 18px;
}

.right img {
  max-width: 160px;
  height: auto;
}

button {
  border: 0;
  color: white;
  padding: 8px 12px;
  border-radius: 8px;
}
</style>
