<template>
  <view class="component-section navigator-container">
    <view class="title">1. navigator</view>
    <view class="description">页面链接，用于跳转到应用内的某个页面。</view>
    <view class="example">
      <navigator url="/pages/home/home" open-type="navigate">跳转到首页</navigator>
    </view>
    <view class="usage">
      <view class="usage-title">使用案例：</view>
      <view class="code">
<pre>
&lt;navigator url="/pages/home/home" open-type="navigate"&gt;跳转到首页&lt;/navigator&gt;
</pre>
      </view>
    </view>
    <view class="api">
      <view class="api-title">常用属性：</view>
      <view class="api-content">
        <view>url: 应用内的跳转链接</view>
        <view>open-type: 跳转方式</view>
        <view>delta: 当 open-type 为 'navigateBack' 时有效，表示回退的层数</view>
        <view>hover-class: 指定点击时的样式类</view>
      </view>
    </view>
  </view>
</template>

<script>
export default {
  name: 'NavigatorContainer'
}
</script>

<style scoped>
.component-section {
  background-color: #ffffff;
  border-radius: 8px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  margin-bottom: 20px;
  padding: 20px;
  border-top: 5px solid #3F51B5;
}

.title {
  font-size: 28px;
  font-weight: bold;
  color: #3F51B5;
  margin-bottom: 15px;
  padding-bottom: 10px;
  border-bottom: 2px solid #3F51B5;
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
  background-color: #E8EAF6;
  border-radius: 8px;
}

.example navigator {
  display: inline-block;
  padding: 10px 15px;
  background-color: #3F51B5;
  color: white;
  border-radius: 4px;
  text-decoration: none;
}

.usage {
  margin: 20px 0;
}

.usage-title {
  font-weight: bold;
  margin-bottom: 10px;
  font-size: 18px;
  color: #3F51B5;
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
  background-color: #C5CAE9;
  padding: 15px;
  border-radius: 8px;
  margin-top: 20px;
}

.api-title {
  font-weight: bold;
  margin-bottom: 10px;
  font-size: 18px;
  color: #3F51B5;
}

.api-content {
  background-color: #ffffff;
  padding: 10px;
  border-radius: 4px;
  font-size: 14px;
  line-height: 1.5;
}
</style>
