<template>
  aaa
  <!-- 表示される -->
  <Feature :is-feature="isFeatureFlugAdminPage">
    <HelloWorld msg="hoge" />
  </Feature>

  <!-- 表示されない -->
  <Feature :is-feature="isFeatureFlugSignUp">
    <HelloWorld msg="fuga" />
  </Feature>
</template>

<script>
import HelloWorldVue from "./components/HelloWorld.vue";
import Feature from "./components/Feature.vue";
import { isFeatureFlugSignUp, isFeatureFlugAdminPage } from "./feature";
import { defineComponent } from "vue";

export default defineComponent({
  name: "App",
  components: {
    HelloWorld: HelloWorldVue,
    Feature,
  },

  setup() {
    return {
      isFeatureFlugSignUp,
      isFeatureFlugAdminPage,
    };
  },
});
</script>

<style>
</style>
