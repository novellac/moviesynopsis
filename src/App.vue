<template>
  <BaseInput
    label="Name"
    :model-value="myInput"
    @update:model-value="myInput = $event"
  />
  <code>{{ myInput }}</code>
  <HelloWorld msg="Hello Vue 3 in CodeSandbox!" />
</template>

<script>
import BaseInput from "./components/BaseInput.vue";
import HelloWorldVue from "./components/HelloWorld.vue";
export default {
  name: "App",
  components: {
    BaseInput: BaseInput,
    HelloWorld: HelloWorldVue,
  },
  data() {
    return {
      myInput: "bloop",
    };
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
