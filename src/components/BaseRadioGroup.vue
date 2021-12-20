<template>
  <fieldset>
    <legend>{{ legend }}</legend>
    <BaseRadioButton
      v-for="option in options"
      :key="option.value"
      :label="option.label"
      :groupName="groupName"
      :value="option.value"
      v-bind="$attrs"
    />
  </fieldset>
</template>

<script>
import BaseRadioButton from "./BaseRadioButton.vue";

export default {
  components: {
    BaseRadioButton
  },
  props: {
    options: {
      type: Array,
      default: () => []
    },
    groupName: {
      type: String,
      required: true
    },
    legend: {
      type: String,
      required: true
    }
  }
};
</script>