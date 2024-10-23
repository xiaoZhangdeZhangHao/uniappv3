<template>
  <view class="component-section canvas-container">
    <view class="title">1. canvas</view>
    <view class="description">画布组件，用于绘制图形。</view>
    <view class="example">
      <canvas canvas-id="myCanvas" id="myCanvas" class="canvas-example"></canvas>
      <button @click="drawOnCanvas">在画布上绘制</button>
    </view>
    <view class="usage">
      <view class="usage-title">使用案例：</view>
      <view class="code">
<pre>
&lt;canvas canvas-id="myCanvas" id="myCanvas"&gt;&lt;/canvas&gt;

// 在 script 中
methods: {
  drawOnCanvas() {
    const ctx = uni.createCanvasContext('myCanvas')
    ctx.setFillStyle('red')
    ctx.fillRect(10, 10, 100, 100)
    ctx.draw()
  }
}
</pre>
      </view>
    </view>
    <view class="api">
      <view class="api-title">常用方法：</view>
      <view class="api-content">
        <view>createCanvasContext: 创建 canvas 上下文</view>
        <view>canvasToTempFilePath: 将 canvas 内容保存为图片</view>
        <view>canvasGetImageData: 获取 canvas 区域像素数据</view>
        <view>canvasPutImageData: 将像素数据绘制到 canvas</view>
      </view>
    </view>
  </view>
</template>

<script>
export default {
  name: 'CanvasContainer',
  methods: {
    drawOnCanvas() {
      const ctx = uni.createCanvasContext('myCanvas')
      ctx.setFillStyle('red')
      ctx.fillRect(10, 10, 100, 100)
      ctx.setFillStyle('blue')
      ctx.fillRect(50, 50, 100, 100)
      ctx.setFillStyle('yellow')
      ctx.beginPath()
      ctx.arc(100, 100, 50, 0, 2 * Math.PI)
      ctx.fill()
      ctx.draw()
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

.canvas-example {
  width: 100%;
  height: 200px;
  border: 1px solid #C5CAE9;
  margin-bottom: 10px;
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
