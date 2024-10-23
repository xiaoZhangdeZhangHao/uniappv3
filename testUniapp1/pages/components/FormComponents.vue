<template>
  <view class="form-components">
    <ButtonContainer />
    <CheckboxContainer />
    <EditorContainer />
    <FormContainer />
    <InputContainer />
    <LabelContainer />
    <PickerContainer />
    <PickerViewContainer />
    <RadioContainer />
    <SliderContainer />
    <SwitchContainer />
    <TextareaContainer />
  </view>
</template>

<script>
import ButtonContainer from './ButtonContainer.vue'
import CheckboxContainer from './CheckboxContainer.vue'
import EditorContainer from './EditorContainer.vue'
import FormContainer from './FormContainer.vue'
import InputContainer from './InputContainer.vue'
import LabelContainer from './LabelContainer.vue'
import PickerContainer from './PickerContainer.vue'
import PickerViewContainer from './PickerViewContainer.vue'
import RadioContainer from './RadioContainer.vue'
import SliderContainer from './SliderContainer.vue'
import SwitchContainer from './SwitchContainer.vue'
import TextareaContainer from './TextareaContainer.vue'

export default {
  name: 'FormComponents',
  components: {
    ButtonContainer,
    CheckboxContainer,
    EditorContainer,
    FormContainer,
    InputContainer,
    LabelContainer,
    PickerContainer,
    PickerViewContainer,
    RadioContainer,
    SliderContainer,
    SwitchContainer,
    TextareaContainer
  }
}
</script>

<style>
.form-components {
  padding: 20px;
  background-color: #f8f8f8;
}
</style>
