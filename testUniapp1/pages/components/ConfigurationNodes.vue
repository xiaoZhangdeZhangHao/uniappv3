<template>
  <view class="configuration-nodes">
    <view class="component-section">
      <view class="title">配置节点</view>
      <view class="description">配置节点用于设置应用程序的全局配置或页面级别的配置。</view>
      
      <view class="config-item">
        <view class="subtitle">1. page-meta</view>
        <view class="description">页面属性配置节点，用于指定页面的一些属性、监听页面事件。</view>
        <view class="usage">
          <view class="usage-title">使用案例：</view>
          <view class="code">
<pre>
&lt;page-meta
  :background-text-style="bgTextStyle"
  :background-color="bgColor"
  :background-color-top="bgColorTop"
  :background-color-bottom="bgColorBottom"
  :scroll-top="scrollTop"
  page-style="color: green"
&gt;
  &lt;navigation-bar
    title="导航栏标题"
    loading="true"
    front-color="#ffffff"
    background-color="#000000"
  /&gt;
&lt;/page-meta&gt;
</pre>
          </view>
        </view>
      </view>

      <view class="config-item">
        <view class="subtitle">2. navigation-bar</view>
        <view class="description">导航条配置节点，用于指定导航栏的一些属性。</view>
        <view class="usage">
          <view class="usage-title">使用案例：</view>
          <view class="code">
<pre>
&lt;navigation-bar
  title="导航栏标题"
  loading="true"
  front-color="#ffffff"
  background-color="#000000"
/&gt;
</pre>
          </view>
        </view>
      </view>

      <view class="config-item">
        <view class="subtitle">3. pages.json</view>
        <view class="description">应用的全局配置文件，用于配置页面路由、窗口样式、tabBar 等。</view>
        <view class="usage">
          <view class="usage-title">使用案例：</view>
          <view class="code">
<pre>
{
  "pages": [
    {
      "path": "pages/index/index",
      "style": {
        "navigationBarTitleText": "首页"
      }
    }
  ],
  "globalStyle": {
    "navigationBarTextStyle": "black",
    "navigationBarTitleText": "UniApp示例",
    "navigationBarBackgroundColor": "#F8F8F8",
    "backgroundColor": "#F8F8F8"
  },
  "tabBar": {
    "color": "#7A7E83",
    "selectedColor": "#3cc51f",
    "borderStyle": "black",
    "backgroundColor": "#ffffff",
    "list": [{
      "pagePath": "pages/index/index",
      "iconPath": "static/tab_home.png",
      "selectedIconPath": "static/tab_home_active.png",
      "text": "首页"
    }, {
      "pagePath": "pages/my/my",
      "iconPath": "static/tab_my.png",
      "selectedIconPath": "static/tab_my_active.png",
      "text": "我的"
    }]
  }
}
</pre>
          </view>
        </view>
      </view>
    </view>
  </view>
</template>

<script>
export default {
  name: 'ConfigurationNodes'
}
</script>

<style scoped>
.configuration-nodes {
  padding: 20px;
  background-color: #f8f8f8;
}

.component-section {
  background-color: #ffffff;
  border-radius: 8px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  margin-bottom: 20px;
  padding: 20px;
  border-top: 5px solid #9C27B0;
}

.title {
  font-size: 28px;
  font-weight: bold;
  color: #9C27B0;
  margin-bottom: 15px;
  padding-bottom: 10px;
  border-bottom: 2px solid #9C27B0;
  text-shadow: 1px 1px 2px rgba(0,0,0,0.1);
}

.description {
  font-size: 16px;
  color: #333;
  margin-bottom: 20px;
  line-height: 1.5;
}

.config-item {
  margin-bottom: 30px;
}

.subtitle {
  font-size: 22px;
  font-weight: bold;
  color: #9C27B0;
  margin-bottom: 10px;
}

.usage {
  margin: 20px 0;
}

.usage-title {
  font-weight: bold;
  margin-bottom: 10px;
  font-size: 18px;
  color: #9C27B0;
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
</style>
