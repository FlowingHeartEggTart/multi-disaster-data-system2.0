<template>
  <div class="content">
    <!-- 数据图表区域 -->
    <div class="card chart-area">
      <div class="card-header">
        <i class="fas fa-chart-line card-icon"></i>
        <h2>数据图表可视化</h2>
      </div>
      <div class="chart-content">
        <span>图表加载中...</span>
      </div>
    </div>

    <!-- 实时新闻 -->
    <div class="card news-section">
      <div class="card-header">
        <i class="fas fa-newspaper card-icon"></i>
        <h2>实时新闻</h2>
      </div>
      <ul>
        <li><i class="fas fa-bullhorn"></i> 地震救援进展...</li>
        <li><i class="fas fa-cloud"></i> 最新灾情更新...</li>
        <li><i class="fas fa-leaf"></i> 气象变化预测...</li>
      </ul>
    </div>

    <!-- 关于我们模块 -->
    <div class="card about-us">
      <div class="card-header">
        <i class="fas fa-info-circle card-icon"></i>
        <h2>关于我们</h2>
      </div>
      <div class="about-content">
        <p>想了解更多关于我们的信息？点击下面的按钮！</p>
        <button class="about-btn" @click="goToAboutPage">
          了解更多
        </button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Content',
  methods: {
    goToAboutPage() {
      // 跳转到“关于我们”页面，假设路由路径为 '/about'
      this.$router.push('/about');
    },
  },
};
</script>

<style scoped>
.content {
  display: flex;
  flex-direction: column;
  gap: 30px;
  padding: 20px;
  flex: 1;
  overflow-y: auto;
}

/* 卡片样式 */
.card {
  background: rgba(255, 255, 255, 0.1);
  backdrop-filter: blur(10px);
  border-radius: 15px;
  padding: 20px;
  box-shadow: 0 4px 15px rgba(0, 0, 0, 0.3);
  transition: transform 0.3s, box-shadow 0.3s;
}

.card:hover {
  transform: translateY(-5px);
  box-shadow: 0 6px 20px rgba(0, 0, 0, 0.4);
}

/* 卡片头部 */
.card-header {
  display: flex;
  align-items: center;
  gap: 10px;
  margin-bottom: 15px;
}

.card-icon {
  font-size: 24px;
  color: #1abc9c;
}

.card h2 {
  font-size: 20px;
  color: #ffffff;
  margin: 0;
}

/* 数据图表内容 */
.chart-content {
  height: 300px;
  background: rgba(255, 255, 255, 0.2);
  border-radius: 10px;
  display: flex;
  justify-content: center;
  align-items: center;
  color: #ffffff;
  font-weight: bold;
}

/* 实时新闻 */
.news-section ul {
  list-style: none;
  padding: 0;
  margin: 0;
  color: #ffffff;
}

.news-section li {
  margin: 8px 0;
  font-size: 16px;
  display: flex;
  align-items: center;
  gap: 10px;
}

/* 关于我们 */
.about-content {
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: center;
}

.about-content p {
  color: #ffffff;
  margin-bottom: 15px;
}

.about-btn {
  padding: 10px 20px;
  border: none;
  background-color: #1abc9c;
  color: #ffffff;
  font-size: 16px;
  font-weight: bold;
  border-radius: 5px;
  cursor: pointer;
  transition: background-color 0.3s ease, transform 0.3s ease;
}

.about-btn:hover {
  background-color: #16a085;
  transform: scale(1.05);
}
</style>
