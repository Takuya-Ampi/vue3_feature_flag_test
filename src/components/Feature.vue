<template>
  <template v-if="isFeature">
    <slot></slot>
  </template>
</template>

<script>
export default {
  props: {
    isFeature: Boolean,
  },
};
</script>
