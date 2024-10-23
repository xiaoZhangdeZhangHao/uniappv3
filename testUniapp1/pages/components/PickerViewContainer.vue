<template>
  <view class="component-section picker-view-container">
    <view class="title">8. picker-view</view>
    <view class="description">嵌入页面的滚动选择器。</view>
    <view class="example">
      <picker-view :indicator-style="indicatorStyle" :value="value" @change="bindChange">
        <picker-view-column>
          <view v-for="(item, index) in years" :key="index">{{item}}年</view>
        </picker-view-column>
        <picker-view-column>
          <view v-for="(item, index) in months" :key="index">{{item}}月</view>
        </picker-view-column>
        <picker-view-column>
          <view v-for="(item, index) in days" :key="index">{{item}}日</view>
        </picker-view-column>
      </picker-view>
    </view>
    <view class="usage">
      <view class="usage-title">使用案例：</view>
      <view class="code">
<pre>
&lt;picker-view :indicator-style="indicatorStyle" :value="value" @change="bindChange"&gt;
  &lt;picker-view-column&gt;
    &lt;view v-for="(item, index) in years" :key="index"&gt;{{item}}年&lt;/view&gt;
  &lt;/picker-view-column&gt;
  &lt;picker-view-column&gt;
    &lt;view v-for="(item, index) in months" :key="index"&gt;{{item}}月&lt;/view&gt;
  &lt;/picker-view-column&gt;
  &lt;picker-view-column&gt;
    &lt;view v-for="(item, index) in days" :key="index"&gt;{{item}}日&lt;/view&gt;
  &lt;/picker-view-column&gt;
&lt;/picker-view&gt;
</pre>
      </view>
    </view>
    <view class="api">
      <view class="api-title">常用属性：</view>
      <view class="api-content">
        <view>value: 数组中的数字依次表示 picker-view 内的 picker-view-column 选择的第几项</view>
        <view>indicator-style: 设置选择器中间选中框的样式</view>
        <view>@change: 当滚动选择，value 改变时触发 change 事件</view>
      </view>
    </view>
  </view>
</template>

<script>
export default {
  name: 'PickerViewContainer',
  data() {
    const date = new Date()
    const years = []
    const months = []
    const days = []
    for (let i = 1990; i <= date.getFullYear(); i++) {
      years.push(i)
    }
    for (let i = 1; i <= 12; i++) {
      months.push(i)
    }
    for (let i = 1; i <= 31; i++) {
      days.push(i)
    }
    return {
      years,
      months,
      days,
      value: [9999, 1, 1],
      indicatorStyle: `height: 50px;`
    }
  },
  methods: {
    bindChange(e) {
      const val = e.detail.value
      console.log('picker-view发送选择改变，携带值为', val)
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
  border-top: 5px solid #009688;
}

.title {
  font-size: 28px;
  font-weight: bold;
  color: #009688;
  margin-bottom: 15px;
  padding-bottom: 10px;
  border-bottom: 2px solid #009688;
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
  background-color: #E0F2F1;
  border-radius: 8px;
}

.usage {
  margin: 20px 0;
}

.usage-title {
  font-weight: bold;
  margin-bottom: 10px;
  font-size: 18px;
  color: #009688;
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
  background-color: #B2DFDB;
  padding: 15px;
  border-radius: 8px;
  margin-top: 20px;
}

.api-title {
  font-weight: bold;
  margin-bottom: 10px;
  font-size: 18px;
  color: #009688;
}

.api-content {
  background-color: #ffffff;
  padding: 10px;
  border-radius: 4px;
  font-size: 14px;
  line-height: 1.5;
}
</style>
