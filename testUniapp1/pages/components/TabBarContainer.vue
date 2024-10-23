<template>
  <view class="component-section tabbar-container">
    <view class="title">2. tabBar</view>
    <view class="description">底部导航栏，用于在不同页面之间进行切换。</view>
    <view class="example">
      <view class="tabbar-example">
        <view class="tabbar-item" v-for="(item, index) in tabBarItems" :key="index">
          {{ item.text }}
        </view>
      </view>
    </view>
    <view class="usage">
      <view class="usage-title">使用案例：</view>
      <view class="code">
<pre>
// 在 pages.json 中配置
"tabBar": {
  "color": "#7A7E83",
  "selectedColor": "#3cc51f",
  "borderStyle": "black",
  "backgroundColor": "#ffffff",
  "list": [{
    "pagePath": "pages/index/index",
    "iconPath": "static/image/icon_component.png",
    "selectedIconPath": "static/image/icon_component_HL.png",
    "text": "组件"
  }, {
    "pagePath": "pages/API/index",
    "iconPath": "static/image/icon_API.png",
    "selectedIconPath": "static/image/icon_API_HL.png",
    "text": "接口"
  }]
}
</pre>
      </view>
    </view>
    <view class="api">
      <view class="api-title">常用属性：</view>
      <view class="api-content">
        <view>color: tab 上的文字默认颜色</view>
        <view>selectedColor: tab 上的文字选中时的颜色</view>
        <view>backgroundColor: tab 的背景色</view>
        <view>borderStyle: tabbar 上边框的颜色</view>
        <view>list: tab 的列表，详见上方的配置</view>
      </view>
    </view>
  </view>
</template>

<script>
export default {
  name: 'TabBarContainer',
  data() {
    return {
      tabBarItems: [
        { text: '首页' },
        { text: '分类' },
        { text: '购物车' },
        { text: '我的' }
      ]
    }
  }
}
</script>

<style scoped>
.component-section {
  background-color: #ffffff;
  border-radius: 8px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  margin-bottom: 20px;
  padding: 20px;
  border-top: 5px solid #FF9800;
}

.title {
  font-size: 28px;
  font-weight: bold;
  color: #FF9800;
  margin-bottom: 15px;
  padding-bottom: 10px;
  border-bottom: 2px solid #FF9800;
  text-shadow: 1px 1px 2px rgba(0,0,0,0.1);
}

.description {
  font-size: 16px;
  color: #333;
  margin-bottom: 20px;
  line-height: 1.5;
}

.example {
  margin: 20px 0;
  padding: 15px;
  background-color: #FFF3E0;
  border-radius: 8px;
}

.tabbar-example {
  display: flex;
  justify-content: space-around;
  background-color: #fff;
  padding: 10px 0;
  border-top: 1px solid #e0e0e0;
}

.tabbar-item {
  text-align: center;
  font-size: 14px;
  color: #333;
}

.usage {
  margin: 20px 0;
}

.usage-title {
  font-weight: bold;
  margin-bottom: 10px;
  font-size: 18px;
  color: #FF9800;
}

.code {
  background-color: #f0f0f0;
  padding: 15px;
  border-radius: 8px;
  font-family: monospace;
  white-space: pre-wrap;
  word-break: break-all;
  font-size: 14px;
  line-height: 1.5;
  overflow-x: auto;
}

.api {
  background-color: #FFE0B2;
  padding: 15px;
  border-radius: 8px;
  margin-top: 20px;
}

.api-title {
  font-weight: bold;
  margin-bottom: 10px;
  font-size: 18px;
  color: #FF9800;
}

.api-content {
  background-color: #ffffff;
  padding: 10px;
  border-radius: 4px;
  font-size: 14px;
  line-height: 1.5;
}
</style>
