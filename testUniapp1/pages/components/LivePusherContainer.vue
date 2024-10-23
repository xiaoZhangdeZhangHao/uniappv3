<template>
  <view class="component-section live-pusher-container">
    <view class="title">7. live-pusher</view>
    <view class="description">实时音视频录制组件。</view>
    <view class="example">
      <live-pusher url="rtmp://test.aliyun.com/live/test" mode="SD" :muted="false" :enable-camera="true" :auto-focus="true" :beauty="1" whiteness="2"></live-pusher>
    </view>
    <view class="usage">
      <view class="usage-title">使用案例：</view>
      <view class="code">
<pre>
&lt;live-pusher
  url="rtmp://test.aliyun.com/live/test"
  mode="SD"
  :muted="false"
  :enable-camera="true"
  :auto-focus="true"
  :beauty="1"
  whiteness="2"
&gt;&lt;/live-pusher&gt;
</pre>
      </view>
    </view>
    <view class="api">
      <view class="api-title">常用属性：</view>
      <view class="api-content">
        <view>url: 推流地址</view>
        <view>mode: 推流视频模式</view>
        <view>muted: 是否静音</view>
        <view>enable-camera: 是否开启摄像头</view>
        <view>auto-focus: 是否自动对焦</view>
        <view>beauty: 美颜程度，取值范围 0-9</view>
        <view>whiteness: 美白程度，取值范围 0-9</view>
      </view>
    </view>
  </view>
</template>

<script>
export default {
  name: 'LivePusherContainer'
}
</script>

<style scoped>
.component-section {
  background-color: #ffffff;
  border-radius: 8px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  margin-bottom: 20px;
  padding: 20px;
  border-top: 5px solid #00BCD4;
}

.title {
  font-size: 28px;
  font-weight: bold;
  color: #00BCD4;
  margin-bottom: 15px;
  padding-bottom: 10px;
  border-bottom: 2px solid #00BCD4;
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
  background-color: #E0F7FA;
  border-radius: 8px;
}

.usage {
  margin: 20px 0;
}

.usage-title {
  font-weight: bold;
  margin-bottom: 10px;
  font-size: 18px;
  color: #00BCD4;
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
  background-color: #B2EBF2;
  padding: 15px;
  border-radius: 8px;
  margin-top: 20px;
}

.api-title {
  font-weight: bold;
  margin-bottom: 10px;
  font-size: 18px;
  color: #00BCD4;
}

.api-content {
  background-color: #ffffff;
  padding: 10px;
  border-radius: 4px;
  font-size: 14px;
  line-height: 1.5;
}
</style>
