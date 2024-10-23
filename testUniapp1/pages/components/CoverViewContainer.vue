<template>
  <view class="component-section cover-view-container">
    <view class="title">6. cover-view</view>
    <view class="description">覆盖在原生组件上的文本视图，可覆盖在 video、map 等原生组件上。</view>
    <view class="example">
      <view class="native-component-simulator">
        <cover-view class="cover-text">覆盖的文本</cover-view>
      </view>
    </view>
    <view class="usage">
      <view class="usage-title">使用案例：</view>
      <view class="code">
<pre>
&lt;video src="video-url"&gt;
  &lt;cover-view class="controls"&gt;
    &lt;cover-view class="play" @click="play"&gt;播放&lt;/cover-view&gt;
    &lt;cover-view class="pause" @click="pause"&gt;暂停&lt;/cover-view&gt;
  &lt;/cover-view&gt;
&lt;/video&gt;
</pre>
      </view>
    </view>
    <view class="api">
      <view class="api-title">常用属性：</view>
      <view class="api-content">
        <view>scroll-top: 设置顶部滚动偏移量</view>
      </view>
    </view>
  </view>
</template>

<script>
export default {
  name: 'CoverViewContainer'
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

.native-component-simulator {
  position: relative;
  height: 150px;
  background-color: #B2EBF2;
  border-radius: 4px;
}

.cover-text {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  background-color: rgba(0, 188, 212, 0.7);
  color: white;
  padding: 10px;
  border-radius: 4px;
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
