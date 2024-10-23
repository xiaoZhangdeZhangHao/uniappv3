<template>
  <view class="component-section button-container">
    <view class="title">1. button</view>
    <view class="description">按钮组件，用于触发操作。</view>
    <view class="example">
      <button>默认按钮</button>
      <button type="primary">主要按钮</button>
      <button type="warn">警告按钮</button>
      <button disabled>禁用按钮</button>
    </view>
    <view class="usage">
      <view class="usage-title">使用案例：</view>
      <view class="code">
<pre>
&lt;button&gt;默认按钮&lt;/button&gt;
&lt;button type="primary"&gt;主要按钮&lt;/button&gt;
&lt;button type="warn"&gt;警告按钮&lt;/button&gt;
&lt;button disabled&gt;禁用按钮&lt;/button&gt;
</pre>
      </view>
    </view>
    <view class="api">
      <view class="api-title">常用属性：</view>
      <view class="api-content">
        <view>size: 按钮的大小</view>
        <view>type: 按钮的样式类型</view>
        <view>plain: 按钮是否镂空</view>
        <view>disabled: 是否禁用</view>
        <view>loading: 名称前是否带 loading 图标</view>
      </view>
    </view>
  </view>
</template>

<script>
export default {
  name: 'ButtonContainer'
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
}

.example button {
  margin-right: 10px;
  margin-bottom: 10px;
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
