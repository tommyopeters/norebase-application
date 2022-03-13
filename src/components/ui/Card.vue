<template>
  <div class="card" @click="hasBanner" :class="classes">
    <div class="card-banner" v-if="hasBanner">
      <slot name="card-banner"></slot>
    </div>
    <div class="card-header" v-if="hasHeader">
      <slot name="card-header"></slot>
    </div>
    <div class="card-body">
      <slot></slot>
    </div>
    <div class="card-footer" v-if="hasFooter">
      <slot name="card-footer"></slot>
    </div>
  </div>
</template>

<script>
export default {
  props: ["classes"],
  computed: {
    hasBanner: function() {
      return !!this.$slots["card-banner"];
    },
    hasHeader: function() {
      return !!this.$slots["card-header"];
    },
    hasFooter: function() {
      return !!this.$slots["card-footer"];
    },
  },
};
</script>

<style></style>
