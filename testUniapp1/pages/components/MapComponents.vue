<template>
  <view class="map-components">
    <MapContainer />
  </view>
</template>

<script>
import MapContainer from './MapContainer.vue'

export default {
  name: 'MapComponents',
  components: {
    MapContainer
  }
}
</script>

<style>
.map-components {
  padding: 20px;
  background-color: #f8f8f8;
}
</style>
