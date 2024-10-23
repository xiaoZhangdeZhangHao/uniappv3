<template>
  <view class="component-section match-media-container">
    <view class="title">4. match-media</view>
    <view class="description">屏幕动态适配组件，用于动态适配不同尺寸的屏幕。</view>
    <view class="example">
      <match-media min-width="400" max-width="700">
        <view class="match-media-demo">
          This content is visible when screen width is between 400px and 700px
        </view>
      </match-media>
    </view>
    <view class="usage">
      <view class="usage-title">使用案例：</view>
      <view class="code">
<pre>
&lt;match-media :min-width="375" :max-width="768"&gt;
  &lt;view&gt;在 375px 到 768px 宽度的设备上显示&lt;/view&gt;
&lt;/match-media&gt;
&lt;match-media :min-width="769"&gt;
  &lt;view&gt;在宽度大于 769px 的设备上显示&lt;/view&gt;
&lt;/match-media&gt;
</pre>
      </view>
    </view>
    <view class="api">
      <view class="api-title">常用属性：</view>
      <view class="api-content">
        <view>min-width: 最小宽度（px）</view>
        <view>max-width: 最大宽度（px）</view>
        <view>width: 宽度（px）</view>
        <view>min-height: 最小高度（px）</view>
        <view>max-height: 最大高度（px）</view>
        <view>height: 高度（px）</view>
      </view>
    </view>
  </view>
</template>

<script>
export default {
  name: 'MatchMediaContainer'
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

.match-media-demo {
  background-color: #E1BEE7;
  color: #9C27B0;
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
