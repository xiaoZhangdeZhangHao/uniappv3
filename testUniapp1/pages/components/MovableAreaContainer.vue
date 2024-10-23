<template>
  <view class="component-section movable-area-container">
    <view class="title">5. movable-area</view>
    <view class="description">可移动的视图容器，用于指定 movable-view 的可移动区域。</view>
    <view class="example">
      <movable-area class="movable-example">
        <movable-view class="movable-view" direction="all">可移动</movable-view>
      </movable-area>
    </view>
    <view class="usage">
      <view class="usage-title">使用案例：</view>
      <view class="code">
<pre>
&lt;movable-area style="height: 200px; width: 200px; background: #ccc;"&gt;
  &lt;movable-view style="height: 50px; width: 50px; background: blue;" direction="all"&gt;
    可拖动视图
  &lt;/movable-view&gt;
&lt;/movable-area&gt;
</pre>
      </view>
    </view>
    <view class="api">
      <view class="api-title">movable-view 常用属性：</view>
      <view class="api-content">
        <view>direction: 移动方向，all | vertical | horizontal | none</view>
        <view>inertia: 是否带有惯性</view>
        <view>out-of-bounds: 是否允许超出边界</view>
      </view>
    </view>
  </view>
</template>

<script>
export default {
  name: 'MovableAreaContainer'
}
</script>

<style scoped>
.component-section {
  background-color: #ffffff;
  border-radius: 8px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  margin-bottom: 20px;
  padding: 20px;
  border-top: 5px solid #F44336;
}

.title {
  font-size: 28px;
  font-weight: bold;
  color: #F44336;
  margin-bottom: 15px;
  padding-bottom: 10px;
  border-bottom: 2px solid #F44336;
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
  background-color: #FFEBEE;
  border-radius: 8px;
}

.movable-example {
  height: 200px;
  width: 200px;
  background-color: #FFCDD2;
  border-radius: 4px;
}

.movable-view {
  height: 50px;
  width: 50px;
  background-color: #F44336;
  color: white;
  display: flex;
  justify-content: center;
  align-items: center;
  border-radius: 4px;
}

.usage {
  margin: 20px 0;
}

.usage-title {
  font-weight: bold;
  margin-bottom: 10px;
  font-size: 18px;
  color: #F44336;
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
  background-color: #FFCDD2;
  padding: 15px;
  border-radius: 8px;
  margin-top: 20px;
}

.api-title {
  font-weight: bold;
  margin-bottom: 10px;
  font-size: 18px;
  color: #F44336;
}

.api-content {
  background-color: #ffffff;
  padding: 10px;
  border-radius: 4px;
  font-size: 14px;
  line-height: 1.5;
}
</style>
