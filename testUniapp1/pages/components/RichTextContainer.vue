<template>
  <view class="component-section rich-text-container">
    <view class="title">3. rich-text</view>
    <view class="description">富文本组件，用于显示 HTML 内容。</view>
    <view class="example">
      <rich-text :nodes="nodes"></rich-text>
    </view>
    <view class="usage">
      <view class="usage-title">使用案例：</view>
      <view class="code">
<pre>
&lt;rich-text :nodes="nodes"&gt;&lt;/rich-text&gt;

// 在 script 中
data() {
  return {
    nodes: [{
      name: 'div',
      attrs: {
        class: 'div-class',
        style: 'color: red;'
      },
      children: [{
        type: 'text',
        text: 'Hello Rich-Text!'
      }]
    }]
  }
}
</pre>
      </view>
    </view>
    <view class="api">
      <view class="api-title">常用属性：</view>
      <view class="api-content">
        <view>nodes: 节点列表 / HTML String</view>
      </view>
    </view>
  </view>
</template>

<script>
export default {
  name: 'RichTextContainer',
  data() {
    return {
      nodes: [{
        name: 'div',
        attrs: {
          class: 'div-class',
          style: 'color: red;'
        },
        children: [{
          type: 'text',
          text: 'Hello Rich-Text!'
        }]
      }]
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
  border-top: 5px solid #FF9800;
}

.title {
  font-size: 28px;
  font-weight: bold;
  color: #FF9800;
  margin-bottom: 15px;
  padding-bottom: 10px;
  border-bottom: 2px solid #FF9800;
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
  background-color: #FFF3E0;
  border-radius: 8px;
}

.usage {
  margin: 20px 0;
}

.usage-title {
  font-weight: bold;
  margin-bottom: 10px;
  font-size: 18px;
  color: #FF9800;
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
  background-color: #FFE0B2;
  padding: 15px;
  border-radius: 8px;
  margin-top: 20px;
}

.api-title {
  font-weight: bold;
  margin-bottom: 10px;
  font-size: 18px;
  color: #FF9800;
}

.api-content {
  background-color: #ffffff;
  padding: 10px;
  border-radius: 4px;
  font-size: 14px;
  line-height: 1.5;
}
</style>
