<template>
  <view class="component-section scroll-view-container">
    <view class="title">2. scroll-view</view>
    <view class="description">可滚动视图区域，用于区域滚动。</view>
    <view class="example">
      <scroll-view class="scroll-view-example" scroll-y>
        <view v-for="i in 20" :key="i" class="scroll-item">项目 {{ i }}</view>
      </scroll-view>
    </view>
    <view class="usage">
      <view class="usage-title">使用案例：</view>
      <view class="code">
<pre>
&lt;scroll-view scroll-y="true" class="scroll-view" @scrolltoupper="upper" @scrolltolower="lower"&gt;
  &lt;view v-for="(item, index) in items" :key="index" class="scroll-item"&gt;
    {{ item }}
  &lt;/view&gt;
&lt;/scroll-view&gt;
</pre>
      </view>
    </view>
    <view class="api">
      <view class="api-title">常用属性：</view>
      <view class="api-content">
        <view>scroll-x: 允许横向滚动</view>
        <view>scroll-y: 允许纵向滚动</view>
        <view>scroll-top: 设置竖向滚动条位置</view>
        <view>scroll-left: 设置横向滚动条位置</view>
      </view>
    </view>
  </view>
</template>

<script>
export default {
  name: 'ScrollViewContainer'
}
</script>

<style scoped>
.component-section {
  background-color: #ffffff;
  border-radius: 8px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  margin-bottom: 20px;
  padding: 20px;
  border-top: 5px solid #2196F3;
}

.title {
  font-size: 28px;
  font-weight: bold;
  color: #2196F3;
  margin-bottom: 15px;
  padding-bottom: 10px;
  border-bottom: 2px solid #2196F3;
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
  background-color: #E3F2FD;
  border-radius: 8px;
}

.scroll-view-example {
  height: 200px;
  border: 1px solid #2196F3;
  border-radius: 4px;
}

.scroll-item {
  height: 40px;
  line-height: 40px;
  text-align: center;
  border-bottom: 1px solid #E3F2FD;
}

.usage {
  margin: 20px 0;
}

.usage-title {
  font-weight: bold;
  margin-bottom: 10px;
  font-size: 18px;
  color: #2196F3;
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
  background-color: #BBDEFB;
  padding: 15px;
  border-radius: 8px;
  margin-top: 20px;
}

.api-title {
  font-weight: bold;
  margin-bottom: 10px;
  font-size: 18px;
  color: #2196F3;
}

.api-content {
  background-color: #ffffff;
  padding: 10px;
  border-radius: 4px;
  font-size: 14px;
  line-height: 1.5;
}
</style>
