<template>
  <view class="component-section switch-container">
    <view class="title">11. switch</view>
    <view class="description">开关选择器。</view>
    <view class="example">
      <switch checked @change="switchChange" />
    </view>
    <view class="usage">
      <view class="usage-title">使用案例：</view>
      <view class="code">
<pre>
&lt;switch checked @change="switchChange" /&gt;
</pre>
      </view>
    </view>
    <view class="api">
      <view class="api-title">常用属性：</view>
      <view class="api-content">
        <view>checked: 是否选中</view>
        <view>disabled: 是否禁用</view>
        <view>type: 样式，有效值：switch, checkbox</view>
        <view>color: switch 的颜色，同 css 的 color</view>
        <view>@change: checked 改变时触发 change 事件</view>
      </view>
    </view>
  </view>
</template>

<script>
export default {
  name: 'SwitchContainer',
  methods: {
    switchChange(e) {
      console.log('switch发生change事件，携带值为', e.detail.value)
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
  border-top: 5px solid #8BC34A;
}

.title {
  font-size: 28px;
  font-weight: bold;
  color: #8BC34A;
  margin-bottom: 15px;
  padding-bottom: 10px;
  border-bottom: 2px solid #8BC34A;
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
  background-color: #F1F8E9;
  border-radius: 8px;
}

.usage {
  margin: 20px 0;
}

.usage-title {
  font-weight: bold;
  margin-bottom: 10px;
  font-size: 18px;
  color: #8BC34A;
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
  background-color: #DCEDC8;
  padding: 15px;
  border-radius: 8px;
  margin-top: 20px;
}

.api-title {
  font-weight: bold;
  margin-bottom: 10px;
  font-size: 18px;
  color: #8BC34A;
}

.api-content {
  background-color: #ffffff;
  padding: 10px;
  border-radius: 4px;
  font-size: 14px;
  line-height: 1.5;
}
</style>
