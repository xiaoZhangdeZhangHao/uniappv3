<template>
  <view class="component-section map-container">
    <view class="title">1. map</view>
    <view class="description">地图组件，用于展示地图。</view>
    <view class="example">
      <map
        style="width: 100%; height: 300px;"
        :latitude="latitude"
        :longitude="longitude"
        :markers="markers"
      ></map>
    </view>
    <view class="usage">
      <view class="usage-title">使用案例：</view>
      <view class="code">
<pre>
&lt;map
  style="width: 100%; height: 300px;"
  :latitude="latitude"
  :longitude="longitude"
  :markers="markers"
&gt;&lt;/map&gt;

// 在 script 中
data() {
  return {
    latitude: 39.909,
    longitude: 116.39742,
    markers: [{
      id: 1,
      latitude: 39.909,
      longitude: 116.39742,
      title: '北京'
    }]
  }
}
</pre>
      </view>
    </view>
    <view class="api">
      <view class="api-title">常用属性：</view>
      <view class="api-content">
        <view>latitude: 中心纬度</view>
        <view>longitude: 中心经度</view>
        <view>scale: 缩放级别，默认为16</view>
        <view>markers: 标记点</view>
        <view>show-location: 显示带有方向的当前定位点</view>
        <view>@tap: 点击地图时触发</view>
      </view>
    </view>
  </view>
</template>

<script>
export default {
  name: 'MapContainer',
  data() {
    return {
      latitude: 39.909,
      longitude: 116.39742,
      markers: [{
        id: 1,
        latitude: 39.909,
        longitude: 116.39742,
        title: '北京'
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
