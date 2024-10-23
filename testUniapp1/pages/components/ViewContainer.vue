<template>
  <view class="component-section view-container">
    <view class="title">1. view</view>
    <view class="description">视图容器，类似于 HTML 中的 div，用于包裹各种元素内容。</view>
    <view class="example">
      <view class="view-example red">红色 view</view>
      <view class="view-example blue">蓝色 view</view>
      <view class="view-example green">绿色 view</view>
    </view>
    <view class="usage">
      <view class="usage-title">使用案例：</view>
      <view class="code">
<pre>
&lt;view class="container"&gt;
  &lt;view class="item" hover-class="hover-item"&gt;
    这是一个可点击的 view
  &lt;/view&gt;
  &lt;view class="item" hover-stop-propagation&gt;
    这个 view 阻止事件冒泡
  &lt;/view&gt;
&lt;/view&gt;
</pre>
      </view>
    </view>
    <view class="api">
      <view class="api-title">常用属性：</view>
      <view class="api-content">
        <view>hover-class: 指定按下去的样式类</view>
        <view>hover-stop-propagation: 阻止冒泡</view>
      </view>
    </view>
  </view>
</template>

<script>
export default {
  name: 'ViewContainer'
}
</script>

<style scoped>
.component-section {
  background-color: #ffffff;
  border-radius: 8px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  margin-bottom: 20px;
  padding: 20px;
  border-top: 5px solid #4CAF50;
}

.title {
  font-size: 28px;
  font-weight: bold;
  color: #4CAF50;
  margin-bottom: 15px;
  padding-bottom: 10px;
  border-bottom: 2px solid #4CAF50;
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
  background-color: #E8F5E9;
  border-radius: 8px;
}

.view-example {
  padding: 10px;
  margin-bottom: 10px;
  color: white;
  border-radius: 4px;
}

.red { background-color: #ff6666; }
.blue { background-color: #6666ff; }
.green { background-color: #66ff66; }

.usage {
  margin: 20px 0;
}

.usage-title {
  font-weight: bold;
  margin-bottom: 10px;
  font-size: 18px;
  color: #4CAF50;
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
  background-color: #C8E6C9;
  padding: 15px;
  border-radius: 8px;
  margin-top: 20px;
}

.api-title {
  font-weight: bold;
  margin-bottom: 10px;
  font-size: 18px;
  color: #4CAF50;
}

.api-content {
  background-color: #ffffff;
  padding: 10px;
  border-radius: 4px;
  font-size: 14px;
  line-height: 1.5;
}
</style>
