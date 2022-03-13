<template>
  <li class="sidebar-list" :class="text == 'Home' ? 'active' : ''">
    <span class="icon" v-html="icon"> </span>
    <span>{{ text }}</span>
  </li>
</template>

<script>
export default {
  props: ["text", "icon"],
};
</script>

<style></style>
