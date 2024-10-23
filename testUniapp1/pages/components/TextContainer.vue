<template>
  <view class="component-section text-container">
    <view class="title">2. text</view>
    <view class="description">文本组件，用于显示文本内容。</view>
    <view class="example">
      <text>这是一个普通文本</text>
      <text selectable>这是一个可选择的文本</text>
      <text space="ensp">这是一个 ensp 空格文本</text>
      <text decode>&gt; 解码文本 &lt;</text>
    </view>
    <view class="usage">
      <view class="usage-title">使用案例：</view>
      <view class="code">
<pre>
&lt;text&gt;普通文本&lt;/text&gt;
&lt;text selectable&gt;可选择文本&lt;/text&gt;
&lt;text space="ensp"&gt;ensp 空格文本&lt;/text&gt;
&lt;text decode&gt;&amp;gt; 解码文本 &amp;lt;&lt;/text&gt;
</pre>
      </view>
    </view>
    <view class="api">
      <view class="api-title">常用属性：</view>
      <view class="api-content">
        <view>selectable: 文本是否可选</view>
        <view>space: 显示连续空格的方式</view>
        <view>decode: 是否解码文本</view>
      </view>
    </view>
  </view>
</template>

<script>
export default {
  name: 'TextContainer'
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

.example text {
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
