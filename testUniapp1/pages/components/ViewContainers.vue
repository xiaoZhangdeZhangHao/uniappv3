<template>
  <view class="view-containers">
    <ViewContainer />
    <ScrollViewContainer />
    <SwiperContainer />
    <MatchMediaContainer />
    <MovableAreaContainer />
    <CoverViewContainer />
    <CoverImageContainer />
  </view>
</template>

<script>
import ViewContainer from './ViewContainer.vue'
import ScrollViewContainer from './ScrollViewContainer.vue'
import SwiperContainer from './SwiperContainer.vue'
import MatchMediaContainer from './MatchMediaContainer.vue'
import MovableAreaContainer from './MovableAreaContainer.vue'
import CoverViewContainer from './CoverViewContainer.vue'
import CoverImageContainer from './CoverImageContainer.vue'

export default {
  name: 'ViewContainers',
  components: {
    ViewContainer,
    ScrollViewContainer,
    SwiperContainer,
    MatchMediaContainer,
    MovableAreaContainer,
    CoverViewContainer,
    CoverImageContainer
  }
}
</script>

<style>
.view-containers {
  padding: 20px;
  background-color: #f8f8f8;
}

.component-section {
  background-color: #ffffff;
  border-radius: 8px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  margin-bottom: 20px;
  padding: 20px;
  border-top: 5px solid;
}

.title {
  font-size: 24px;
  font-weight: bold;
  margin-bottom: 10px;
  padding-bottom: 5px;
  border-bottom: 2px solid;
}

.description {
  font-size: 16px;
  color: #333;
  margin-bottom: 15px;
}

.example {
  margin: 15px 0;
  padding: 10px;
  border-radius: 4px;
}

.usage {
  margin: 15px 0;
}

.usage-title {
  font-weight: bold;
  margin-bottom: 5px;
}

.code {
  background-color: #f0f0f0;
  padding: 10px;
  border-radius: 4px;
  font-family: monospace;
  white-space: pre-wrap;
  word-break: break-all;
  font-size: 14px;
}

.api {
  padding: 10px;
  border-radius: 4px;
  margin-top: 15px;
}

.api-title {
  font-weight: bold;
  margin-bottom: 5px;
}

/* 特定组件样式 */
.view-container .component-section {
  border-top-color: #4CAF50;
}
.view-container .title {
  color: #4CAF50;
  border-bottom-color: #4CAF50;
}
.view-container .example {
  background-color: #E8F5E9;
}
.view-container .api {
  background-color: #C8E6C9;
}

.scroll-view-container .component-section {
  border-top-color: #2196F3;
}
.scroll-view-container .title {
  color: #2196F3;
  border-bottom-color: #2196F3;
}
.scroll-view-container .example {
  background-color: #E3F2FD;
}
.scroll-view-container .api {
  background-color: #BBDEFB;
}

.swiper-container .component-section {
  border-top-color: #FF9800;
}
.swiper-container .title {
  color: #FF9800;
  border-bottom-color: #FF9800;
}
.swiper-container .example {
  background-color: #FFF3E0;
}
.swiper-container .api {
  background-color: #FFE0B2;
}

.match-media-container .component-section {
  border-top-color: #9C27B0;
}
.match-media-container .title {
  color: #9C27B0;
  border-bottom-color: #9C27B0;
}
.match-media-container .example {
  background-color: #F3E5F5;
}
.match-media-container .api {
  background-color: #E1BEE7;
}

.movable-area-container .component-section {
  border-top-color: #F44336;
}
.movable-area-container .title {
  color: #F44336;
  border-bottom-color: #F44336;
}
.movable-area-container .example {
  background-color: #FFEBEE;
}
.movable-area-container .api {
  background-color: #FFCDD2;
}

.cover-view-container .component-section {
  border-top-color: #00BCD4;
}
.cover-view-container .title {
  color: #00BCD4;
  border-bottom-color: #00BCD4;
}
.cover-view-container .example {
  background-color: #E0F7FA;
}
.cover-view-container .api {
  background-color: #B2EBF2;
}

.cover-image-container .component-section {
  border-top-color: #FFC107;
}
.cover-image-container .title {
  color: #FFC107;
  border-bottom-color: #FFC107;
}
.cover-image-container .example {
  background-color: #FFF8E1;
}
.cover-image-container .api {
  background-color: #FFECB3;
}
</style>
