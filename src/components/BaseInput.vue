<template>
  <label :for="`${label}-input`">
    {{ label }}
  </label>
  <input
    :id="label"
    type="text"
    :value="modelValue"
    @input="$emit('update:modelValue', $event.target.value)"
  />
</template>

<script>
export default {
  props: ["modelValue", "label"],
  emits: ["update:modelValue"],
};
</script>