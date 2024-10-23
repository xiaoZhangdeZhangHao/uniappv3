<template>
  <view class="component-section editor-container">
    <view class="title">3. editor</view>
    <view class="description">富文本编辑器，可以对图片、文字进行编辑。</view>
    <view class="example">
      <editor id="editor" class="editor"></editor>
    </view>
    <view class="usage">
      <view class="usage-title">使用案例：</view>
      <view class="code">
<pre>
&lt;editor id="editor" class="editor" @ready="onEditorReady"&gt;&lt;/editor&gt;

// 在 script 中
methods: {
  onEditorReady() {
    uni.createSelectorQuery().select('#editor').context((res) => {
      this.editorCtx = res.context
    }).exec()
  }
}
</pre>
      </view>
    </view>
    <view class="api">
      <view class="api-title">常用方法：</view>
      <view class="api-content">
        <view>insertDivider: 插入分割线</view>
        <view>insertImage: 插入图片</view>
        <view>insertText: 插入文本</view>
        <view>setContents: 初始化编辑器内容</view>
        <view>getContents: 获取编辑器内容</view>
      </view>
    </view>
  </view>
</template>

<script>
export default {
  name: 'EditorContainer',
  data() {
    return {
      editorCtx: null
    }
  },
  mounted() {
    this.$nextTick(() => {
      this.initEditor();
    });
  },
  methods: {
    initEditor() {
      const query = uni.createSelectorQuery().in(this);
      query.select('#editor').context((res) => {
        if (res && res.context) {
          this.editorCtx = res.context;
        } else {
          console.error('Failed to get editor context');
        }
      }).exec();
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

.example {
  margin: 20px 0;
  padding: 15px;
  background-color: #F3E5F5;
  border-radius: 8px;
}

.editor {
  border: 1px solid #ccc;
  min-height: 200px;
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

.api {
  background-color: #E1BEE7;
  padding: 15px;
  border-radius: 8px;
  margin-top: 20px;
}

.api-title {
  font-weight: bold;
  margin-bottom: 10px;
  font-size: 18px;
  color: #9C27B0;
}

.api-content {
  background-color: #ffffff;
  padding: 10px;
  border-radius: 4px;
  font-size: 14px;
  line-height: 1.5;
}
</style>
