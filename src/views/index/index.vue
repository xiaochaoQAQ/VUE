<script>
export default {
  data() {
    return {
      // 设置轮播切换的时间间隔，单位为毫秒
      carouselInterval: 3000, // 每3秒切换一次
    };
  },
};
</script>


<template>
  <div class="block text-center">
    <el-carousel height="200px" motion-blur>
      <el-carousel-item v-for="item in 4" :key="item">
      </el-carousel-item>
    </el-carousel>
  </div>
</template>

<style scoped>
.demonstration {
  color: var(--el-text-color-secondary);
}


.el-carousel__item {
  color: #475669;
  opacity: 0.75;
}

.el-carousel__item:nth-child(1) {
  background-color: #99a9bf;
  background-image: url("../../assets/bgi1.jpg"); /* First background image */
  background-size: cover; /* Ensure the background image covers the entire area */
  background-position: center;
}

.el-carousel__item:nth-child(2) {
  background-color: #d3dce6;
  background-image: url("../../assets/bgi2.jpg"); /* Second background image */
  background-size: cover;
  background-position: center;
}

.el-carousel__item:nth-child(3) {
  background-color: #f0f0f0;
  background-image: url("../../assets/bgi3.jpg"); /* Third background image */
  background-size: cover;
  background-position: center;
}

.el-carousel__item:nth-child(4) {
  background-color: #ffe0b2;
  background-image: url("../../assets/bgi4.jpg"); /* Fourth background image */
  background-size: cover;
  background-position: center;
}

</style>
