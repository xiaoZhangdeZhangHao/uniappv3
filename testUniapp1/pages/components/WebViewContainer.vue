<template>
  <view class="component-section webview-container">
    <view class="title">1. web-view</view>
    <view class="description">承载网页的容器，会自动铺满整个页面。</view>
    <view class="example">
      <button @click="openWebView">打开 Web-view</button>
    </view>
    <view class="usage">
      <view class="usage-title">使用案例：</view>
      <view class="code">
<pre>
&lt;web-view :src="url"&gt;&lt;/web-view&gt;

// 在 script 中
data() {
  return {
    url: 'https://www.baidu.com'
  }
}
</pre>
      </view>
    </view>
    <view class="api">
      <view class="api-title">常用属性：</view>
      <view class="api-content">
        <view>src: 指向网页的链接</view>
        <view>@message: 网页向应用 postMessage 时，会在特定时机（后退、组件销毁、分享）触发并收到消息</view>
      </view>
    </view>
  </view>
</template>

<script>
export default {
  name: 'WebViewContainer',
  methods: {
    openWebView() {
      uni.navigateTo({
        url: '/pages/webview/webview?url=https://www.baidu.com'
      })
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

