<template>
  <view class="component-section animation-view-container">
    <view class="title">1. animation-view</view>
    <view class="description">动画组件，用于播放由 BodyMovin 导出的 AE 动画。</view>
    <view class="example">
      <view class="animation-view-placeholder">
        动画视图占位符
      </view>
    </view>
    <view class="usage">
      <view class="usage-title">使用案例：</view>
      <view class="code">
<pre>
&lt;animation-view
  :path="animationData"
  :loop="true"
  :autoplay="true"
  @bindended="onAnimationEnd"
/&gt;
</pre>
      </view>
    </view>
    <view class="api">
      <view class="api-title">常用属性：</view>
      <view class="api-content">
        <view>path: 动画资源地址</view>
        <view>loop: 是否循环播放</view>
        <view>autoplay: 是否自动播放</view>
        <view>action: 动画操作，可选值：play、pause、stop</view>
      </view>
    </view>
  </view>
</template>

<script>
export default {
  name: 'AnimationViewContainer'
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

.animation-view-placeholder {
  height: 200px;
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: #E1BEE7;
  color: #9C27B0;
  font-weight: bold;
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
