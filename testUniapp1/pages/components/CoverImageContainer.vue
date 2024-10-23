<template>
  <view class="component-section cover-image-container">
    <view class="title">7. cover-image</view>
    <view class="description">覆盖在原生组件上的图片视图，可覆盖在 video、map 等原生组件上。</view>
    <view class="example">
      <view class="native-component-simulator">
        <cover-image src="/static/logo.png" class="cover-image"></cover-image>
      </view>
    </view>
    <view class="usage">
      <view class="usage-title">使用案例：</view>
      <view class="code">
        &lt;map&gt;
          &lt;cover-image
            class="logo"
            src="/static/logo.png"
            @click="handleClick"
          &gt;&lt;/cover-image&gt;
        &lt;/map&gt;
      </view>
    </view>
    <view class="api">
      <view class="api-title">常用属性：</view>
      <view class="api-content">
        <view>src: 图片路径</view>
      </view>
    </view>
  </view>
</template>

<script>
export default {
  name: 'CoverImageContainer'
}
</script>

<style scoped>
.component-section {
  background-color: #ffffff;
  border-radius: 8px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  margin-bottom: 20px;
  padding: 20px;
  border-top: 5px solid #FFC107;
}

.title {
  font-size: 28px;
  font-weight: bold;
  color: #FFC107;
  margin-bottom: 15px;
  padding-bottom: 10px;
  border-bottom: 2px solid #FFC107;
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
  background-color: #FFF8E1;
  border-radius: 8px;
}

.native-component-simulator {
  position: relative;
  height: 150px;
  background-color: #FFECB3;
  border-radius: 4px;
}

.cover-image {
  position: absolute;
  top: 10px;
  left: 10px;
  width: 50px;
  height: 50px;
}

.usage {
  margin: 20px 0;
}

.usage-title {
  font-weight: bold;
  margin-bottom: 10px;
  font-size: 18px;
  color: #FFC107;
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
  background-color: #FFECB3;
  padding: 15px;
  border-radius: 8px;
  margin-top: 20px;
}

.api-title {
  font-weight: bold;
  margin-bottom: 10px;
  font-size: 18px;
  color: #FFC107;
}

.api-content {
  background-color: #ffffff;
  padding: 10px;
  border-radius: 4px;
  font-size: 14px;
  line-height: 1.5;
}
</style>
