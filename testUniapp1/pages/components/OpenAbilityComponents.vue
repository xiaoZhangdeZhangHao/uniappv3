<template>
  <view class="open-ability-components">
    <WebViewContainer />
    <AdContainer />
    <OfficialAccountContainer />
    <OpenDataContainer />
  </view>
</template>

<script>
import WebViewContainer from './WebViewContainer.vue'
import AdContainer from './AdContainer.vue'
import OfficialAccountContainer from './OfficialAccountContainer.vue'
import OpenDataContainer from './OpenDataContainer.vue'

export default {
  name: 'OpenAbilityComponents',
  components: {
    WebViewContainer,
    AdContainer,
    OfficialAccountContainer,
    OpenDataContainer
  }
}
</script>

<style>
.open-ability-components {
  padding: 20px;
  background-color: #f8f8f8;
}
</style>
