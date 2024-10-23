<template>
  <view class="component-section live-player-container">
    <view class="title">6. live-player</view>
    <view class="description">直播播放组件。</view>
    <view class="example">
      <live-player src="https://domain/pull_stream" mode="live" :autoplay="false" :muted="true" :orientation="vertical" object-fit="contain"></live-player>
    </view>
    <view class="usage">
      <view class="usage-title">使用案例：</view>
      <view class="code">
<pre>
&lt;live-player
  src="https://domain/pull_stream"
  mode="live"
  :autoplay="false"
  :muted="true"
  orientation="vertical"
  object-fit="contain"
&gt;&lt;/live-player&gt;
</pre>
      </view>
    </view>
    <view class="api">
      <view class="api-title">常用属性：</view>
      <view class="api-content">
        <view>src: 音视频地址</view>
        <view>mode: live（直播），RTC（实时通话，该模式时延更低）</view>
        <view>autoplay: 自动播放</view>
        <view>muted: 是否静音</view>
        <view>orientation: 画面方向</view>
        <view>object-fit: 填��模式</view>
      </view>
    </view>
  </view>
</template>

<script>
export default {
  name: 'LivePlayerContainer'
}
</script>

<style scoped>
.component-section {
  background-color: #ffffff;
  border-radius: 8px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  margin-bottom: 20px;
  padding: 20px;
  border-top: 5px solid #F44336;
}

.title {
  font-size: 28px;
  font-weight: bold;
  color: #F44336;
  margin-bottom: 15px;
  padding-bottom: 10px;
  border-bottom: 2px solid #F44336;
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
  background-color: #FFEBEE;
  border-radius: 8px;
}

.usage {
  margin: 20px 0;
}

.usage-title {
  font-weight: bold;
  margin-bottom: 10px;
  font-size: 18px;
  color: #F44336;
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
  background-color: #FFCDD2;
  padding: 15px;
  border-radius: 8px;
  margin-top: 20px;
}

.api-title {
  font-weight: bold;
  margin-bottom: 10px;
  font-size: 18px;
  color: #F44336;
}

.api-content {
  background-color: #ffffff;
  padding: 10px;
  border-radius: 4px;
  font-size: 14px;
  line-height: 1.5;
}
</style>
