<template>
  <view class="component-section form-container">
    <view class="title">4. form</view>
    <view class="description">表单，将组件内的用户输入提交。</view>
    <view class="example">
      <form @submit="formSubmit" @reset="formReset">
        <input name="input" placeholder="这是一个输入框" />
        <button form-type="submit">Submit</button>
        <button form-type="reset">Reset</button>
      </form>
    </view>
    <view class="usage">
      <view class="usage-title">使用案例：</view>
      <view class="code">
<pre>
&lt;form @submit="formSubmit" @reset="formReset"&gt;
  &lt;input name="input" placeholder="这是一个输入框" /&gt;
  &lt;button form-type="submit"&gt;Submit&lt;/button&gt;
  &lt;button form-type="reset"&gt;Reset&lt;/button&gt;
&lt;/form&gt;
</pre>
      </view>
    </view>
    <view class="api">
      <view class="api-title">常用属性：</view>
      <view class="api-content">
        <view>report-submit: 是否返回 formId 用于发送模板消息</view>
      </view>
    </view>
  </view>
</template>

<script>
export default {
  name: 'FormContainer',
  methods: {
    formSubmit(e) {
      console.log('form发生了submit事件，携带数据为：', e.detail.value)
    },
    formReset(e) {
      console.log('form发生了reset事件')
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

.example form {
  display: flex;
  flex-direction: column;
  gap: 10px;
}

.example input {
  padding: 5px;
  border: 1px solid #ddd;
  border-radius: 4px;
}

.example button {
  padding: 5px 10px;
  background-color: #FF5722;
  color: white;
  border: none;
  border-radius: 4px;
  cursor: pointer;
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
