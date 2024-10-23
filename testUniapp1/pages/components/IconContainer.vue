<template>
  <view class="component-section icon-container">
    <view class="title">1. icon</view>
    <view class="description">图标组件，用于展示各种图标。</view>
    <view class="example">
      <icon type="success" size="30" />
      <icon type="info" size="30" />
      <icon type="warn" size="30" color="red" />
    </view>
    <view class="usage">
      <view class="usage-title">使用案例：</view>
      <view class="code">
<pre>
&lt;icon type="success" size="30" /&gt;
&lt;icon type="info" size="30" /&gt;
&lt;icon type="warn" size="30" color="red" /&gt;
</pre>
      </view>
    </view>
    <view class="api">
      <view class="api-title">常用属性：</view>
      <view class="api-content">
        <view>type: 图标类型</view>
        <view>size: 图标大小</view>
        <view>color: 图标颜色</view>
      </view>
    </view>
  </view>
</template>

<script>
export default {
  name: 'IconContainer'
}
</script>

<style scoped>
.component-section {
  background-color: #ffffff;
  border-radius: 8px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  margin-bottom: 20px;
  padding: 20px;
  border-top: 5px solid #3498db;
}

.title {
  font-size: 28px;
  font-weight: bold;
  color: #3498db;
  margin-bottom: 15px;
  padding-bottom: 10px;
  border-bottom: 2px solid #3498db;
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
  background-color: #ecf0f1;
  border-radius: 8px;
  display: flex;
  justify-content: space-around;
}

.usage {
  margin: 20px 0;
}

.usage-title {
  font-weight: bold;
  margin-bottom: 10px;
  font-size: 18px;
  color: #3498db;
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
  background-color: #e8f6fe;
  padding: 15px;
  border-radius: 8px;
  margin-top: 20px;
}

.api-title {
  font-weight: bold;
  margin-bottom: 10px;
  font-size: 18px;
  color: #3498db;
}

.api-content {
  background-color: #ffffff;
  padding: 10px;
  border-radius: 4px;
  font-size: 14px;
  line-height: 1.5;
}
</style>
