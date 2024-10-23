<template>
  <view class="basic-contents">
    <IconContainer />
    <TextContainer />
    <RichTextContainer />
    <ProgressContainer />
  </view>
</template>

<script>
import IconContainer from './IconContainer.vue'
import TextContainer from './TextContainer.vue'
import RichTextContainer from './RichTextContainer.vue'
import ProgressContainer from './ProgressContainer.vue'

export default {
  name: 'BasicContents',
  components: {
    IconContainer,
    TextContainer,
    RichTextContainer,
    ProgressContainer
  }
}
</script>

<style>
.basic-contents {
  padding: 20px;
  background-color: #f8f8f8;
}
</style>
