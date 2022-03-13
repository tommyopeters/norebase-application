<template>
  <div class="author">
    <div class="image-control author-image">
      <img :src="authorImg" alt="" />
    </div>
    <div class="author-details">
      <div class="author-name">{{ authorName }}</div>
      <div class="date">{{ date }}</div>
    </div>
  </div>
</template>

<script>
export default {
  props: ["authorImg", "authorName", "date"],
};
</script>

<style></style>
