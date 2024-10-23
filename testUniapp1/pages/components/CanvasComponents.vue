<template>
  <view class="canvas-components">
    <CanvasContainer />
  </view>
</template>

<script>
import CanvasContainer from './CanvasContainer.vue'

export default {
  name: 'CanvasComponents',
  components: {
    CanvasContainer
  }
}
</script>

<style>
.canvas-components {
  padding: 20px;
  background-color: #f8f8f8;
}
</style>
