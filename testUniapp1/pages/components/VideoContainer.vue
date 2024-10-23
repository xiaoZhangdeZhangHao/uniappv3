<template>
  <view class="component-section video-container">
    <view class="title">5. video</view>
    <view class="description">视频播放组件。</view>
    <view class="example">
      <video :src="videoSrc" controls></video>
    </view>
    <view class="usage">
      <view class="usage-title">使用案例：</view>
      <view class="code">
<pre>
&lt;video
  src="https://example.com/video.mp4"
  autoplay
  loop
  muted
  initial-time="0"
  controls
  @play="onPlay"
  @pause="onPause"
  @ended="onEnded"
&gt;&lt;/video&gt;
</pre>
      </view>
    </view>
    <view class="api">
      <view class="api-title">常用属性：</view>
      <view class="api-content">
        <view>src: 要播放视频的资源地址</view>
        <view>autoplay: 是否自动播放</view>
        <view>loop: 是否循环播放</view>
        <view>muted: 是否静音播放</view>
        <view>initial-time: 指定视频初始播放位置</view>
        <view>controls: 是否显示默认播放控件</view>
        <view>@play: 当开始/继续播放时触发play事件</view>
        <view>@pause: 当暂停播放时触发pause事件</view>
        <view>@ended: 当播放到末尾时触发ended事件</view>
      </view>
    </view>
  </view>
</template>

<script>
export default {
  name: 'VideoContainer',
  data() {
    return {
      videoSrc: 'https://bjetxgzv.cdn.bspapp.com/VKCEYUGU-uni-app-doc/360e4b20-4f2d-11eb-b680-7980c8a877b8.mp4'
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
  border-top: 5px solid #9C27B0;
}

.title {
  font-size: 28px;
  font-weight: bold;
  color: #9C27B0;
  margin-bottom: 15px;
  padding-bottom: 10px;
  border-bottom: 2px solid #9C27B0;
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
  background-color: #F3E5F5;
  border-radius: 8px;
}

.example video {
  width: 100%;
  max-width: 400px;
  display: block;
  margin: 0 auto;
}

.usage {
  margin: 20px 0;
}

.usage-title {
  font-weight: bold;
  margin-bottom: 10px;
  font-size: 18px;
  color: #9C27B0;
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
  background-color: #E1BEE7;
  padding: 15px;
  border-radius: 8px;
  margin-top: 20px;
}

.api-title {
  font-weight: bold;
  margin-bottom: 10px;
  font-size: 18px;
  color: #9C27B0;
}

.api-content {
  background-color: #ffffff;
  padding: 10px;
  border-radius: 4px;
  font-size: 14px;
  line-height: 1.5;
}
</style>
