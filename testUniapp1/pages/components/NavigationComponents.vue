<template>
  <view class="navigation-components">
    <NavigatorContainer />
    <TabBarContainer />
    <NavigationBarContainer />
  </view>
</template>

<script>
import NavigatorContainer from './NavigatorContainer.vue'
import TabBarContainer from './TabBarContainer.vue'
import NavigationBarContainer from './NavigationBarContainer.vue'

export default {
  name: 'NavigationComponents',
  components: {
    NavigatorContainer,
    TabBarContainer,
    NavigationBarContainer
  }
}
</script>

<style>
.navigation-components {
  padding: 20px;
  background-color: #f8f8f8;
}
</style>
