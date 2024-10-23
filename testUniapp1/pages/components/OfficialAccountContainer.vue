<template>
  <view class="component-section official-account-container">
    <view class="title">3. official-account</view>
    <view class="description">公众号关注组件，用于展示公众号关注界面。</view>
    <view class="example">
      <view class="official-account-placeholder">公众号关注组件示例</view>
    </view>
    <view class="usage">
      <view class="usage-title">使用案例：</view>
      <view class="code">
<pre>
&lt;official-account&gt;&lt;/official-account&gt;
</pre>
      </view>
    </view>
    <view class="api">
      <view class="api-title">常用事件：</view>
      <view class="api-content">
        <view>@load: 组件加载成功时触发</view>
        <view>@error: 组件加载失败时触发</view>
      </view>
    </view>
  </view>
</template>

<script>
export default {
  name: 'OfficialAccountContainer'
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

.official-account-placeholder {
  background-color: #C8E6C9;
  color: #4CAF50;
  padding: 20px;
  text-align: center;
  border-radius: 4px;
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
