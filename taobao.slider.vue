<template>
<div class="banner-container full-screen">
  <slider
    :interval="interval"
    :auto-play="autoplay"
    class="slider"
  >
    <div class="frame" v-for="banner in banners" :key="banner.src">
      <image :src="banner.src" class="full-screen"></image>
    </div>
    <indicator
      class="indicator"
    ></indicator>
  </slider>
</div>
</template>

<script>
export default {
  data() {
    return {
      banners: [
        {src: 'https://gw.alicdn.com/imgextra/i1/74/TB2mr70fIyYBuNkSnfoXXcWgVXa_!!74-0-luban.jpg'},
        {src: 'https://aecpm.alicdn.com/simba/img/TB1Y2RPggKTBuNkSne1SuuJoXXa.jpg_q50.jpg'},
        {src: 'https://aecpm.alicdn.com/simba/img/TB14ab1KpXXXXclXFXXSutbFXXX.jpg_q50.jpg'},
        {src: 'https://img.alicdn.com/imgextra/i1/107/TB22lVfgsuYBuNkSmRyXXcA3pXa_!!107-0-luban.jpg'},
        {src: 'https://img.alicdn.com/imgextra/i3/76/TB298tzn7CWBuNjy0FaXXXUlXXa_!!76-0-luban.jpg'},
        {src: 'https://gw.alicdn.com/imgextra/i1/12/TB2.q9Rok9WBuNjSspeXXaz5VXa_!!12-0-lubanu.jpg'},
        {src: 'https://gw.alicdn.com/imgextra/i3/12/TB2B7lsnFuWBuNjSspnXXX1NVXa_!!12-0-lubanu.jpg'},
      ],
      interval: 3000,
      autoplay: true
    }
  }
}
</script>

<style scoped>
.full-screen{
  width: 750px;
  height: 240px;
}
.slider {
  position: relative;
}
.indicator{
  position: absolute;
  item-color: #fff;
  item-selected-color: rgb(255, 80, 0);
  item-size: 16px;
  width: 750px;
  height: 22px;
  bottom: 22px;
}
</style>
