<template>
  <view class="container">
    <view class="header">
      <text>UniApp基础平台</text>
    </view>
    
    <view class="content">
      <scroll-view scroll-x class="tabs">
        <view 
          v-for="(tab, index) in tabs" 
          :key="index" 
          class="tab-item" 
          :class="{ active: currentTab === index }"
          @click="changeTab(index)"
        >
          {{ tab.name }}
        </view>
      </scroll-view>
      
      <scroll-view scroll-y class="tab-content">
        <component :is="tabs[currentTab].component"></component>
      </scroll-view>
    </view>
    
    <view class="footer">
      <text>© 2024 UniApp学习巩固平台</text>
    </view>
  </view>
</template>

<script>
import ViewContainers from '../components/ViewContainers.vue'
import BasicContents from '../components/BasicContents.vue'
import FormComponents from '../components/FormComponents.vue'
import NavigationComponents from '../components/NavigationComponents.vue'
import MediaComponents from '../components/MediaComponents.vue'
import MapComponents from '../components/MapComponents.vue'
import CanvasComponents from '../components/CanvasComponents.vue'
import OpenAbilityComponents from '../components/OpenAbilityComponents.vue'
import ConfigurationNodes from '../components/ConfigurationNodes.vue'

export default {
  components: {
    ViewContainers,
    BasicContents,
    FormComponents,
    NavigationComponents,
    MediaComponents,
    MapComponents,
    CanvasComponents,
    OpenAbilityComponents,
    ConfigurationNodes
  },
  data() {
    return {
      currentTab: 0,
      tabs: [
        { name: '视图容器', component: ViewContainers },
        { name: '基础内容', component: BasicContents },
        { name: '表单组件', component: FormComponents },
        { name: '导航组件', component: NavigationComponents },
        { name: '媒体组件', component: MediaComponents },
        { name: '地图组件', component: MapComponents },
        { name: '画布组件', component: CanvasComponents },
        { name: '开放能力', component: OpenAbilityComponents },
        { name: '配置节点', component: ConfigurationNodes },
      ]
    }
  },
  methods: {
    changeTab(index) {
      this.currentTab = index;
    }
  }
}
</script>

<style>
.container {
  display: flex;
  flex-direction: column;
  height: 100vh;
}

.header {
  background-color: #FF6600;
  color: white;
  padding: 20px;
  text-align: center;
  font-size: 20px;
  font-weight: bold;
}

.content {
  flex: 1;
  display: flex;
  flex-direction: column;
}

.tabs {
  display: flex;
  white-space: nowrap;
  background-color: #f8f8f8;
}

.tab-item {
  display: inline-block;
  padding: 10px 20px;
  font-size: 16px;
  color: #333;
}

.tab-item.active {
  color: #FF6600;
  border-bottom: 2px solid #FF6600;
}

.tab-content {
  flex: 1;
  padding: 20px;
}

.footer {
  background-color: #f8f8f8;
  color: #666;
  padding: 10px;
  text-align: center;
  font-size: 14px;
}
</style>
