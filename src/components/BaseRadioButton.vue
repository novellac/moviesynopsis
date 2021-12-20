<template>
  <label>
    <input
      type="radio"
      :name="groupName"
      :value="value"
      @change="$emit('update:modelValue', $event.target.value)"
    />
    {{ label }}
  </label>
</template>

<script>
export default {
  props: {
    groupName: {
      type: String,
      required: true
    },
    value: {
      type: String,
      required: true
    },
    label: {
      type: String,
      required: true
    }
  }
};
</script>
