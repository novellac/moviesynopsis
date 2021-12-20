<template>
  <p>
    <span class="bold"> {{ one }}&nbsp;{{ two }}</span> finds herself stranded
    in her hometown during a pandemic lockdown, after she came home to
    <span class="bold">{{ three }}</span
    >. Against her better judgement, she falls in love with
    <span class="bold">{{ four }}</span
    >. Together, they learn the true meaning of Christmas.
  </p>
</template>

<script>
export default {
  props: {
    one: {
      type: String,
      default: `[1]`
    },
    two: {
      type: String,
      default: `[2]`
    },
    three: {
      type: String,
      default: `[3]`
    },
    four: {
      type: String,
      default: `[4]`
    }
  }
};
</script>

<style scoped>
.bold {
  font-weight: bold;
}
</style>