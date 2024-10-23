<template>
  <view class="component-section navigationbar-container">
    <view class="title">3. navigationBar</view>
    <view class="description">顶部导航栏，用于显示页面标题和导航按钮。</view>
    <view class="example">
      <view class="navigationbar-example">
        <view class="navigationbar-title">页面标题</view>
      </view>
    </view>
    <view class="usage">
      <view class="usage-title">使用案例：</view>
      <view class="code">
<pre>
// 在 pages.json 中配置
{
  "path": "pages/index/index",
  "style": {
    "navigationBarTitleText": "首页",
    "navigationBarBackgroundColor": "#F8F8F8",
    "navigationBarTextStyle": "black"
  }
}
</pre>
      </view>
    </view>
    <view class="api">
      <view class="api-title">常用属性：</view>
      <view class="api-content">
        <view>navigationBarTitleText: 导航栏标题文字内容</view>
        <view>navigationBarBackgroundColor: 导航栏背景颜色</view>
        <view>navigationBarTextStyle: 导航栏标题颜色及状态栏前景颜色，仅支持 black/white</view>
        <view>navigationStyle: 导航栏样式，仅支持 default/custom。custom 模式可自定义导航栏，只保留右上角胶囊按钮</view>
      </view>
    </view>
  </view>
</template>

<script>
export default {
  name: 'NavigationBarContainer'
}
</script>

<style scoped>
.component-section {
  background-color: #ffffff;
  border-radius: 8px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  margin-bottom: 20px;
  padding: 20px;
  border-top: 5px solid #4CAF50;
}

.title {
  font-size: 28px;
  font-weight: bold;
  color: #4CAF50;
  margin-bottom: 15px;
  padding-bottom: 10px;
  border-bottom: 2px solid #4CAF50;
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
  background-color: #E8F5E9;
  border-radius: 8px;
}

.navigationbar-example {
  background-color: #F8F8F8;
  padding: 10px;
  text-align: center;
  font-size: 18px;
  font-weight: bold;
}

.usage {
  margin: 20px 0;
}

.usage-title {
  font-weight: bold;
  margin-bottom: 10px;
  font-size: 18px;
  color: #4CAF50;
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
  background-color: #C8E6C9;
  padding: 15px;
  border-radius: 8px;
  margin-top: 20px;
}

.api-title {
  font-weight: bold;
  margin-bottom: 10px;
  font-size: 18px;
  color: #4CAF50;
}

.api-content {
  background-color: #ffffff;
  padding: 10px;
  border-radius: 4px;
  font-size: 14px;
  line-height: 1.5;
}
</style>
