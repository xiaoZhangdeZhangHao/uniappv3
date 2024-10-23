<template>
  <view class="component-section input-container">
    <view class="title">5. input</view>
    <view class="description">输入框。</view>
    <view class="example">
      <input placeholder="这是一个输入框" @input="onInput" />
    </view>
    <view class="usage">
      <view class="usage-title">使用案例：</view>
      <view class="code">
<pre>
&lt;input placeholder="这是一个输入框" @input="onInput" /&gt;
</pre>
      </view>
    </view>
    <view class="api">
      <view class="api-title">常用属性：</view>
      <view class="api-content">
        <view>value: 输入框的初始内容</view>
        <view>type: input 的类型</view>
        <view>password: 是否是密码类型</view>
        <view>placeholder: 输入框为空时占位符</view>
        <view>disabled: 是否禁用</view>
      </view>
    </view>
  </view>
</template>

<script>
export default {
  name: 'InputContainer',
  methods: {
    onInput(e) {
      console.log('输入内容：', e.detail.value)
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

.example input {
  width: 100%;
  padding: 10px;
  border: 1px solid #BBDEFB;
  border-radius: 4px;
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
