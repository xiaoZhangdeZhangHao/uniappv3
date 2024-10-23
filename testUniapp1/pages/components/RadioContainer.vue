<template>
  <view class="component-section radio-container">
    <view class="title">9. radio</view>
    <view class="description">单选项目。</view>
    <view class="example">
      <radio-group @change="radioChange">
        <label class="radio" v-for="item in items" :key="item.value">
          <radio :value="item.value" :checked="item.checked" />
          {{item.name}}
        </label>
      </radio-group>
    </view>
    <view class="usage">
      <view class="usage-title">使用案例：</view>
      <view class="code">
<pre>
&lt;radio-group @change="radioChange"&gt;
  &lt;label class="radio" v-for="item in items" :key="item.value"&gt;
    &lt;radio :value="item.value" :checked="item.checked" /&gt;
    <!-- {{item.name}} -->
  &lt;/label&gt;
&lt;/radio-group&gt;
</pre>
      </view>
    </view>
    <view class="api">
      <view class="api-title">常用属性：</view>
      <view class="api-content">
        <view>value: radio 标识。当该 radio 选中时，radio-group 的 change 事件会携带 radio 的 value</view>
        <view>checked: 当前是否选中</view>
        <view>disabled: 是否禁用</view>
        <view>color: radio 的颜色，同 css 的 color</view>
      </view>
    </view>
  </view>
</template>

<script>
export default {
  name: 'RadioContainer',
  data() {
    return {
      items: [
        {value: 'USA', name: '美国'},
        {value: 'CHN', name: '中国', checked: 'true'},
        {value: 'BRA', name: '巴西'},
        {value: 'JPN', name: '日本'},
        {value: 'ENG', name: '英国'},
        {value: 'FRA', name: '法国'},
      ]
    }
  },
  methods: {
    radioChange(e) {
      console.log('radio发生change事件，携带value值为：', e.detail.value)
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
  border-top: 5px solid #673AB7;
}

.title {
  font-size: 28px;
  font-weight: bold;
  color: #673AB7;
  margin-bottom: 15px;
  padding-bottom: 10px;
  border-bottom: 2px solid #673AB7;
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
  background-color: #EDE7F6;
  border-radius: 8px;
}

.radio {
  display: block;
  margin-bottom: 10px;
}

.usage {
  margin: 20px 0;
}

.usage-title {
  font-weight: bold;
  margin-bottom: 10px;
  font-size: 18px;
  color: #673AB7;
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
  background-color: #D1C4E9;
  padding: 15px;
  border-radius: 8px;
  margin-top: 20px;
}

.api-title {
  font-weight: bold;
  margin-bottom: 10px;
  font-size: 18px;
  color: #673AB7;
}

.api-content {
  background-color: #ffffff;
  padding: 10px;
  border-radius: 4px;
  font-size: 14px;
  line-height: 1.5;
}
</style>
