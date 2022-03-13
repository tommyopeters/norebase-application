<template>
  <Card classes="post">
    <template v-slot:card-header>
      <Author
        :authorImg="author.image"
        :authorName="author.name"
        :date="author.date"
      />
    </template>

    <template>
      <h2>{{ title }}</h2>
      <ul class="tags">
        <li v-for="(tag, index) in tags" :key="index" :class="tag.color">
          <span class="hash">#</span>{{ tag.text }}
        </li>
      </ul>
    </template>
    <template v-slot:card-footer>
      <div class="reactions">
        <div class="icon">
          <svg
            xmlns="http://www.w3.org/2000/svg"
            width="24"
            height="24"
            role="img"
            aria-labelledby="ajuduvtig9itcj36c3w4ybpt0err01rb"
            class="crayons-icon"
          >
            <path
              d="M18.884 12.595l.01.011L12 19.5l-6.894-6.894.01-.01A4.875 4.875 0 0112 5.73a4.875 4.875 0 016.884 6.865zM6.431 7.037a3.375 3.375 0 000 4.773L12 17.38l5.569-5.569a3.375 3.375 0 10-4.773-4.773L9.613 10.22l-1.06-1.062 2.371-2.372a3.375 3.375 0 00-4.492.25v.001z"
            ></path>
          </svg>
        </div>
        <spanreactions
          >{{ footer.reactions }}
          <span class="mobile-hide">reactions</span></spanreactions
        >
      </div>
      <div class="comments">
        <div class="icon">
          <svg
            xmlns="http://www.w3.org/2000/svg"
            width="24"
            height="24"
            role="img"
            aria-labelledby="acgagmdomx3bwx4kho2w3z8y9biioqqs"
            class="crayons-icon"
          >
            <path
              d="M10.5 5h3a6 6 0 110 12v2.625c-3.75-1.5-9-3.75-9-8.625a6 6 0 016-6zM12 15.5h1.5a4.501 4.501 0 001.722-8.657A4.5 4.5 0 0013.5 6.5h-3A4.5 4.5 0 006 11c0 2.707 1.846 4.475 6 6.36V15.5z"
            ></path>
          </svg>
        </div>
        <span v-if="footer.comments > 0"
          >{{ footer.comments }} <span class="mobile-hide">comments</span></span
        >
        <span v-else class="mobile-hide">Add Comment</span>
      </div>
      <div class="end">
        <span class="read-time">{{ footer.time }} min read</span>
        <div class="btn btn-grey">Save</div>
      </div>
    </template>
  </Card>
</template>

<script>
import Card from "@/components/ui/Card";
import Author from "@/components/ui/Author";

export default {
  props: ["author", "title", "tags", "footer"],
  components: {
    Card,
    Author,
  },
};
</script>

<style></style>
