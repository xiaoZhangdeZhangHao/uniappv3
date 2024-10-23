<template>
  <view class="component-section ad-container">
    <view class="title">2. ad</view>
    <view class="description">广告组件，用于展示广告。</view>
    <view class="example">
      <view class="ad-placeholder">广告位示例</view>
    </view>
    <view class="usage">
      <view class="usage-title">使用案例：</view>
      <view class="code">
<pre>
&lt;ad unit-id="adunit-XXXXXXXX"&gt;&lt;/ad&gt;
</pre>
      </view>
    </view>
    <view class="api">
      <view class="api-title">常用属性：</view>
      <view class="api-content">
        <view>unit-id: 广告单元id，可在小程序管理后台的流量主模块新建</view>
        <view>ad-type: 广告类型，默认为banner</view>
        <view>@load: 广告加载成功的回调</view>
        <view>@error: 广告加载失败的回调</view>
      </view>
    </view>
  </view>
</template>

<script>
export default {
  name: 'AdContainer'
}
</script>

<style scoped>
.component-section {
  background-color: #ffffff;
  border-radius: 8px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  margin-bottom: 20px;
  padding: 20px;
  border-top: 5px solid #FF5722;
}

.title {
  font-size: 28px;
  font-weight: bold;
  color: #FF5722;
  margin-bottom: 15px;
  padding-bottom: 10px;
  border-bottom: 2px solid #FF5722;
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
  background-color: #FBE9E7;
  border-radius: 8px;
}

.ad-placeholder {
  background-color: #FFCCBC;
  color: #FF5722;
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
  color: #FF5722;
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
  background-color: #FFCCBC;
  padding: 15px;
  border-radius: 8px;
  margin-top: 20px;
}

.api-title {
  font-weight: bold;
  margin-bottom: 10px;
  font-size: 18px;
  color: #FF5722;
}

.api-content {
  background-color: #ffffff;
  padding: 10px;
  border-radius: 4px;
  font-size: 14px;
  line-height: 1.5;
}
</style>
