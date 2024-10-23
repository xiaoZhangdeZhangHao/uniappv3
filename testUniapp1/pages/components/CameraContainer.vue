<template>
  <view class="component-section camera-container">
    <view class="title">3. camera</view>
    <view class="description">系统相机。</view>
    <view class="example">
      <camera device-position="back" flash="auto" @error="error" style="width: 100%; height: 300px;"></camera>
      <button type="primary" @click="takePhoto">拍照</button>
    </view>
    <view class="usage">
      <view class="usage-title">使用案例：</view>
      <view class="code">
<pre>
&lt;camera device-position="back" flash="auto" @error="error" style="width: 100%; height: 300px;"&gt;&lt;/camera&gt;
&lt;button type="primary" @click="takePhoto"&gt;拍照&lt;/button&gt;

// 在 methods 中
takePhoto() {
  const ctx = uni.createCameraContext();
  ctx.takePhoto({
    quality: 'high',
    success: (res) => {
      this.src = res.tempImagePath
    }
  });
}
</pre>
      </view>
    </view>
    <view class="api">
      <view class="api-title">常用属性：</view>
      <view class="api-content">
        <view>device-position: 前置或后置，值为front, back</view>
        <view>flash: 闪光灯，值为auto, on, off</view>
        <view>@error: 用户不允许使用摄像头时触发</view>
      </view>
    </view>
  </view>
</template>

<script>
export default {
  name: 'CameraContainer',
  methods: {
    takePhoto() {
      const ctx = uni.createCameraContext();
      ctx.takePhoto({
        quality: 'high',
        success: (res) => {
          console.log('拍照成功：', res.tempImagePath);
        }
      });
    },
    error(e) {
      console.log(e.detail);
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
