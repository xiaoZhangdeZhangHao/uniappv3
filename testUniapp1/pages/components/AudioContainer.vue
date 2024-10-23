<template>
  <view class="component-section audio-container">
    <view class="title">2. audio</view>
    <view class="description">音频播放组件。</view>
    <view class="example">
      <!-- <audio
        :src="audioSrc"
        :poster="posterSrc"
        :name="audioName"
        :author="audioAuthor"
        controls
      ></audio> -->
    </view>
    <view class="usage">
      <view class="usage-title">使用案例：</view>
      <view class="code">
<pre>
&lt;audio
  :src="audioSrc"
  :poster="posterSrc"
  :name="audioName"
  :author="audioAuthor"
  controls
&gt;&lt;/audio&gt;
</pre>
      </view>
    </view>
    <view class="api">
      <view class="api-title">常用属性：</view>
      <view class="api-content">
        <view>src: 音频资源的地址</view>
        <view>poster: 封面图 URL</view>
        <view>name: 音频名字</view>
        <view>author: 作者名字</view>
        <view>controls: 是否显示默认控件</view>
        <view>loop: 是否循环播放</view>
      </view>
    </view>
  </view>
</template>

<script>
export default {
  name: 'AudioContainer',
  data() {
    return {
      audioSrc: 'https://bjetxgzv.cdn.bspapp.com/VKCEYUGU-hello-uniapp/2cc220e0-c27a-11ea-9dfb-6da8e309e0d8.mp3',
      posterSrc: 'https://bjetxgzv.cdn.bspapp.com/VKCEYUGU-hello-uniapp/7fbf36a0-c27a-11ea-b680-7980c8a877b8.png',
      audioName: '致爱丽丝',
      audioAuthor: '贝多芬'
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

.example audio {
  width: 100%;
  max-width: 300px;
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

.api-content view {
  margin-bottom: 5px;
}
</style>
