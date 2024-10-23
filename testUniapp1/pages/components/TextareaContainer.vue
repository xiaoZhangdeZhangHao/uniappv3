<template>
  <view class="component-section textarea-container">
    <view class="title">12. textarea</view>
    <view class="description">多行输入框。</view>
    <view class="example">
      <textarea @blur="bindTextAreaBlur" auto-height />
    </view>
    <view class="usage">
      <view class="usage-title">使用案例：</view>
      <view class="code">
<pre>
&lt;textarea @blur="bindTextAreaBlur" auto-height /&gt;
</pre>
      </view>
    </view>
    <view class="api">
      <view class="api-title">常用属性：</view>
      <view class="api-content">
        <view>value: 输入框的内容</view>
        <view>placeholder: 输入框为空时占位符</view>
        <view>placeholder-style: 指定 placeholder 的样式</view>
        <view>disabled: 是否禁用</view>
        <view>maxlength: 最大输入长度，设置为 -1 的时候不限制最大长度</view>
        <view>auto-height: 是否自动增高，设置auto-height时，style.height不生效</view>
        <view>@blur: 输入框失去焦点时触发</view>
      </view>
    </view>
  </view>
</template>

<script>
export default {
  name: 'TextareaContainer',
  methods: {
    bindTextAreaBlur(e) {
      console.log('textarea发生blur事件，携带值为', e.detail.value)
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
  border-top: 5px solid #795548;
}

.title {
  font-size: 28px;
  font-weight: bold;
  color: #795548;
  margin-bottom: 15px;
  padding-bottom: 10px;
  border-bottom: 2px solid #795548;
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
  background-color: #EFEBE9;
  border-radius: 8px;
}

.usage {
  margin: 20px 0;
}

.usage-title {
  font-weight: bold;
  margin-bottom: 10px;
  font-size: 18px;
  color: #795548;
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
  background-color: #D7CCC8;
  padding: 15px;
  border-radius: 8px;
  margin-top: 20px;
}

.api-title {
  font-weight: bold;
  margin-bottom: 10px;
  font-size: 18px;
  color: #795548;
}

.api-content {
  background-color: #ffffff;
  padding: 10px;
  border-radius: 4px;
  font-size: 14px;
  line-height: 1.5;
}
</style>
