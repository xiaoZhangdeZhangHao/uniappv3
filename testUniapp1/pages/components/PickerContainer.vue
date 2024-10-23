<template>
  <view class="component-section picker-container">
    <view class="title">7. picker</view>
    <view class="description">从底部弹起的滚动选择器。</view>
    <view class="example">
      <picker :range="array" @change="bindPickerChange">
        <view class="picker">
          当前选择：{{array[index]}}
        </view>
      </picker>
    </view>
    <view class="usage">
      <view class="usage-title">使用案例：</view>
      <view class="code">
<pre>
&lt;picker :range="array" @change="bindPickerChange"&gt;
  &lt;view class="picker"&gt;
    当前选择：{{array[index]}}
  &lt;/view&gt;
&lt;/picker&gt;

// 在 script 中
data() {
  return {
    array: ['美国', '中国', '巴西', '日本'],
    index: 0
  }
},
methods: {
  bindPickerChange(e) {
    console.log('picker发送选择改变，携带值为', e.detail.value)
    this.index = e.detail.value
  }
}
</pre>
      </view>
    </view>
    <view class="api">
      <view class="api-title">常用属性：</view>
      <view class="api-content">
        <view>range: picker 的范围</view>
        <view>value: 当前选择的下标</view>
        <view>@change: value 改变时触发 change 事件</view>
      </view>
    </view>
  </view>
</template>

<script>
export default {
  name: 'PickerContainer',
  data() {
    return {
      array: ['美国', '中国', '巴西', '日本'],
      index: 0
    }
  },
  methods: {
    bindPickerChange(e) {
      console.log('picker发送选择改变，携带值为', e.detail.value)
      this.index = e.detail.value
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
  border-top: 5px solid #E91E63;
}

.title {
  font-size: 28px;
  font-weight: bold;
  color: #E91E63;
  margin-bottom: 15px;
  padding-bottom: 10px;
  border-bottom: 2px solid #E91E63;
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
  background-color: #FCE4EC;
  border-radius: 8px;
}

.usage {
  margin: 20px 0;
}

.usage-title {
  font-weight: bold;
  margin-bottom: 10px;
  font-size: 18px;
  color: #E91E63;
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
  background-color: #F8BBD0;
  padding: 15px;
  border-radius: 8px;
  margin-top: 20px;
}

.api-title {
  font-weight: bold;
  margin-bottom: 10px;
  font-size: 18px;
  color: #E91E63;
}

.api-content {
  background-color: #ffffff;
  padding: 10px;
  border-radius: 4px;
  font-size: 14px;
  line-height: 1.5;
}
</style>
