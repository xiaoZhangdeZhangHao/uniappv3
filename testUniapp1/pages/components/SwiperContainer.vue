<template>
  <view class="component-section swiper-container">
    <view class="title">3. swiper</view>
    <view class="description">滑块视图容器，用于左右滑动或上下滑动切换内容。</view>
    <view class="example">
      <swiper class="swiper-example" indicator-dots autoplay circular>
        <swiper-item v-for="i in 3" :key="i">
          <view class="swiper-item">Swiper 项目 {{ i }}</view>
        </swiper-item>
      </swiper>
    </view>
    <view class="usage">
      <view class="usage-title">使用案例：</view>
      <view class="code">
<pre>
&lt;swiper :indicator-dots="true" :autoplay="true" :interval="3000" :duration="1000"&gt;
  &lt;swiper-item v-for="(item, index) in swiperList" :key="index"&gt;
    &lt;image :src="item.image" mode="aspectFill"&gt;&lt;/image&gt;
  &lt;/swiper-item&gt;
&lt;/swiper&gt;
</pre>
      </view>
    </view>
    <view class="api">
      <view class="api-title">常用属性：</view>
      <view class="api-content">
        <view>indicator-dots: 是否显示面板指示点</view>
        <view>autoplay: 是否自动切换</view>
        <view>interval: 自动切换时间间隔</view>
        <view>circular: 是否采用衔接滑动</view>
      </view>
    </view>
  </view>
</template>

<script>
export default {
  name: 'SwiperContainer'
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

.swiper-example {
  height: 200px;
}

.swiper-item {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100%;
  background-color: #FFE0B2;
  color: #FF9800;
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
