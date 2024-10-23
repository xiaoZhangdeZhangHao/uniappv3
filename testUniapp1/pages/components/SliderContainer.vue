<template>
  <view class="component-section slider-container">
    <view class="title">10. slider</view>
    <view class="description">滑动选择器。</view>
    <view class="example">
      <slider @change="sliderChange" step="5" />
    </view>
    <view class="usage">
      <view class="usage-title">使用案例：</view>
      <view class="code">
<pre>
&lt;slider @change="sliderChange" step="5" /&gt;
</pre>
      </view>
    </view>
    <view class="api">
      <view class="api-title">常用属性：</view>
      <view class="api-content">
        <view>min: 最小值</view>
        <view>max: 最大值</view>
        <view>step: 步长，取值必须大于 0，并且可被(max - min)整除</view>
        <view>disabled: 是否禁用</view>
        <view>value: 当前取值</view>
        <view>@change: 完成一次拖动后触发的事件</view>
      </view>
    </view>
  </view>
</template>

<script>
export default {
  name: 'SliderContainer',
  methods: {
    sliderChange(e) {
      console.log('slider发生change事件，携带值为', e.detail.value)
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
