<template>
  <view class="media-components">
    <AnimationViewContainer />
    <AudioContainer />
    <CameraContainer />
    <ImageContainer />
    <VideoContainer />
    <LivePlayerContainer />
    <LivePusherContainer />
  </view>
</template>

<script>
import AnimationViewContainer from './AnimationViewContainer.vue'
import AudioContainer from './AudioContainer.vue'
import CameraContainer from './CameraContainer.vue'
import ImageContainer from './ImageContainer.vue'
import VideoContainer from './VideoContainer.vue'
import LivePlayerContainer from './LivePlayerContainer.vue'
import LivePusherContainer from './LivePusherContainer.vue'

export default {
  name: 'MediaComponents',
  components: {
    AnimationViewContainer,
    AudioContainer,
    CameraContainer,
    ImageContainer,
    VideoContainer,
    LivePlayerContainer,
    LivePusherContainer
  }
}
</script>

<style>
.media-components {
  padding: 20px;
  background-color: #f8f8f8;
}
</style>
