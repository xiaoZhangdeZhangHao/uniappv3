<template>
  <view class="component-section progress-container">
    <view class="title">4. progress</view>
    <view class="description">进度条组件，用于显示进度。</view>
    <view class="example">
      <progress percent="20" show-info />
      <progress percent="40" stroke-width="12" />
      <progress percent="60" color="pink" />
      <progress percent="80" active />
    </view>
    <view class="usage">
      <view class="usage-title">使用案例：</view>
      <view class="code">
<pre>
&lt;progress percent="20" show-info /&gt;
&lt;progress percent="40" stroke-width="12" /&gt;
&lt;progress percent="60" color="pink" /&gt;
&lt;progress percent="80" active /&gt;
</pre>
      </view>
    </view>
    <view class="api">
      <view class="api-title">常用属性：</view>
      <view class="api-content">
        <view>percent: 百分比 0~100</view>
        <view>show-info: 在进度条右侧显示百分比</view>
        <view>stroke-width: 进度条线的宽度</view>
        <view>color: 进度条颜色</view>
        <view>active: 进度条从左往右的动画</view>
      </view>
    </view>
  </view>
</template>

<script>
export default {
  name: 'ProgressContainer'
}
</script>

<style scoped>
.component-section {
  background-color: #ffffff;
  border-radius: 8px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  margin-bottom: 20px;
  padding: 20px;
  border-top: 5px solid #2196F3;
}

.title {
  font-size: 28px;
  font-weight: bold;
  color: #2196F3;
  margin-bottom: 15px;
  padding-bottom: 10px;
  border-bottom: 2px solid #2196F3;
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
  background-color: #E3F2FD;
  border-radius: 8px;
}

.example progress {
  margin-bottom: 10px;
}

.usage {
  margin: 20px 0;
}

.usage-title {
  font-weight: bold;
  margin-bottom: 10px;
  font-size: 18px;
  color: #2196F3;
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
  background-color: #BBDEFB;
  padding: 15px;
  border-radius: 8px;
  margin-top: 20px;
}

.api-title {
  font-weight: bold;
  margin-bottom: 10px;
  font-size: 18px;
  color: #2196F3;
}

.api-content {
  background-color: #ffffff;
  padding: 10px;
  border-radius: 4px;
  font-size: 14px;
  line-height: 1.5;
}
</style>
