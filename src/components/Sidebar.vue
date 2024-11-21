<template>
  <div class="sidebar">
    <h2>功能菜单</h2>
    <ul>
      <li v-for="item in menuItems" :key="item" @click="handleClick(item)">
        {{ item }}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'Sidebar',
  data() {
    return {
      menuItems: [
        '数据获取',
        '动态窗口设置',
        '震情数据',
        '人员伤亡及失踪',
        '房屋破坏',
        '动态面口设置',
        '灾情智能预测',
        '数据请求管理',
      ],
    };
  },
  methods: {
    handleClick(item) {
      alert(`点击了：${item}`);
    },
  },
};
</script>

<style scoped>
.sidebar {
  width: 250px; /* 固定宽度 */
  background: #2c3e50;
  color: white;
  padding: 20px;
  box-shadow: 2px 0 5px rgba(0, 0, 0, 0.1);
  height: 100%; /* 让菜单栏占满父容器高度 */
}

.sidebar h2 {
  font-size: 18px;
  margin-bottom: 10px;
}

.sidebar ul {
  list-style: none;
  padding: 0;
}

.sidebar li {
  padding: 10px;
  margin: 5px 0;
  cursor: pointer;
  background: #34495e;
  border-radius: 5px;
  text-align: center;
}

.sidebar li:hover {
  background: #1abc9c;
}
</style>
