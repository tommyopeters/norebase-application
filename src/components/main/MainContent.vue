<template>
  <div class="main">
    <div class="filters">
      <div class="btn btn-transparent"><strong>Relevant</strong></div>
      <div class="btn btn-transparent">Latest</div>
      <div class="btn btn-transparent">Top</div>
    </div>
    <Card classes="banner-card post">
      <template v-slot:card-banner>
        <div class="image-control vertical">
          <img src="@/assets/images/banner-1.jpg" alt="" />
        </div>
      </template>
      <template v-slot:card-header>
        <Author
          authorImg="https://res.cloudinary.com/practicaldev/image/fetch/s--0_4vhFoK--/c_fill,f_auto,fl_progressive,h_90,q_auto,w_90/https:/dev-to-uploads.s3.amazonaws.com/uploads/user/profile_image/159737/0315d6fe-95b0-4a0b-87bc-3e907ccc2089.jpg"
          authorName="Madza"
          date="Mar 10"
        />
      </template>
      <template>
        <h2>12 Gorgeous UI Components for Your Design Inspiration</h2>
        <ul class="tags">
          <li class="red"><span class="hash">#</span>webdev</li>
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
            >958 <span class="mobile-hide">reactions</span></spanreactions
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
          <span>64 <span class="mobile-hide">comments</span></span>
        </div>
        <div class="end">
          <span class="read-time">2 min read</span>
          <div class="btn btn-grey">Save</div>
        </div>
      </template>
    </Card>
    <Post
      v-for="(post, index) in posts"
      :key="index"
      :author="post.author"
      :title="post.title"
      :tags="post.tags"
      :footer="post.footer"
    />
  </div>
</template>

<script>
import Post from "@/components/ui/Post";
import Card from "@/components/ui/Card";
import Author from "@/components/ui/Author";
export default {
  components: {
    Card,
    Post,
    Author,
  },

  data() {
    return {
      posts: [
        {
          author: {
            image:
              "https://res.cloudinary.com/practicaldev/image/fetch/s--bzrfhCEs--/c_fill,f_auto,fl_progressive,h_90,q_auto,w_90/https://dev-to-uploads.s3.amazonaws.com/uploads/user/profile_image/530414/941751d8-06b8-41bd-9de9-6ea056b7199f.png",
            name: "Tapajyoti Bose",
            date: "Mar 13",
          },
          title:
            "Automatically Format your code on Git Commit using Husky, ESLint, Prettier in 9 minutes",
          tags: [
            { text: "javascript", color: "yellow" },
            { text: "webdev", color: "purple" },
          ],
          footer: {
            reactions: 3,
            comments: 0,
            time: 5,
          },
        },
        {
          author: {
            image:
              "https://res.cloudinary.com/practicaldev/image/fetch/s--yG9NaJlu--/c_fill,f_auto,fl_progressive,h_90,q_auto,w_90/https://dev-to-uploads.s3.amazonaws.com/uploads/user/profile_image/161327/2ff05281-db58-4dcb-946a-4b679e4a266b.jpeg",
            name: "Alvaro Montoro",
            date: "Mar 13",
          },
          title: "Giving new meanings ot the color functions in CSS",
          tags: [
            { text: "parody", color: "green" },
            { text: "html", color: "blue" },
            { text: "css", color: "red" },
          ],
          footer: {
            reactions: 6,
            comments: 2,
            time: 3,
          },
        },
        {
          author: {
            image:
              "https://res.cloudinary.com/practicaldev/image/fetch/s--s2TtbFus--/c_fill,f_auto,fl_progressive,h_90,q_auto,w_90/https://dev-to-uploads.s3.amazonaws.com/uploads/user/profile_image/480052/f684c523-5316-4ac8-a73e-376d992dbcd4.jpeg",
            name: "Rohith V",
            date: "Mar 13",
          },
          title: "Graph Algorithm - Depth First Search",
          tags: [
            { text: "beginners", color: "green" },
            { text: "programming", color: "blue" },
            { text: "tutorial", color: "red" },
            { text: "career" },
          ],
          footer: {
            reactions: 8,
            comments: 5,
            time: 6,
          },
        },
        {
          author: {
            image:
              "https://res.cloudinary.com/practicaldev/image/fetch/s--bzrfhCEs--/c_fill,f_auto,fl_progressive,h_90,q_auto,w_90/https://dev-to-uploads.s3.amazonaws.com/uploads/user/profile_image/530414/941751d8-06b8-41bd-9de9-6ea056b7199f.png",
            name: "Tapajyoti Bose",
            date: "Mar 13",
          },
          title:
            "Automatically Format your code on Git Commit using Husky, ESLint, Prettier in 9 minutes",
          tags: [
            { text: "javascript", color: "yellow" },
            { text: "webdev", color: "purple" },
          ],
          footer: {
            reactions: 3,
            comments: 0,
            time: 5,
          },
        },
        {
          author: {
            image:
              "https://res.cloudinary.com/practicaldev/image/fetch/s--yG9NaJlu--/c_fill,f_auto,fl_progressive,h_90,q_auto,w_90/https://dev-to-uploads.s3.amazonaws.com/uploads/user/profile_image/161327/2ff05281-db58-4dcb-946a-4b679e4a266b.jpeg",
            name: "Alvaro Montoro",
            date: "Mar 13",
          },
          title: "Giving new meanings ot the color functions in CSS",
          tags: [
            { text: "parody", color: "green" },
            { text: "html", color: "blue" },
            { text: "css", color: "red" },
          ],
          footer: {
            reactions: 6,
            comments: 2,
            time: 3,
          },
        },
        {
          author: {
            image:
              "https://res.cloudinary.com/practicaldev/image/fetch/s--s2TtbFus--/c_fill,f_auto,fl_progressive,h_90,q_auto,w_90/https://dev-to-uploads.s3.amazonaws.com/uploads/user/profile_image/480052/f684c523-5316-4ac8-a73e-376d992dbcd4.jpeg",
            name: "Rohith V",
            date: "Mar 13",
          },
          title: "Graph Algorithm - Depth First Search",
          tags: [
            { text: "beginners", color: "green" },
            { text: "programming", color: "blue" },
            { text: "tutorial", color: "red" },
            { text: "career" },
          ],
          footer: {
            reactions: 8,
            comments: 5,
            time: 6,
          },
        },
        {
          author: {
            image:
              "https://res.cloudinary.com/practicaldev/image/fetch/s--bzrfhCEs--/c_fill,f_auto,fl_progressive,h_90,q_auto,w_90/https://dev-to-uploads.s3.amazonaws.com/uploads/user/profile_image/530414/941751d8-06b8-41bd-9de9-6ea056b7199f.png",
            name: "Tapajyoti Bose",
            date: "Mar 13",
          },
          title:
            "Automatically Format your code on Git Commit using Husky, ESLint, Prettier in 9 minutes",
          tags: [
            { text: "javascript", color: "yellow" },
            { text: "webdev", color: "purple" },
          ],
          footer: {
            reactions: 3,
            comments: 0,
            time: 5,
          },
        },
        {
          author: {
            image:
              "https://res.cloudinary.com/practicaldev/image/fetch/s--yG9NaJlu--/c_fill,f_auto,fl_progressive,h_90,q_auto,w_90/https://dev-to-uploads.s3.amazonaws.com/uploads/user/profile_image/161327/2ff05281-db58-4dcb-946a-4b679e4a266b.jpeg",
            name: "Alvaro Montoro",
            date: "Mar 13",
          },
          title: "Giving new meanings ot the color functions in CSS",
          tags: [
            { text: "parody", color: "green" },
            { text: "html", color: "blue" },
            { text: "css", color: "red" },
          ],
          footer: {
            reactions: 6,
            comments: 2,
            time: 3,
          },
        },
        {
          author: {
            image:
              "https://res.cloudinary.com/practicaldev/image/fetch/s--s2TtbFus--/c_fill,f_auto,fl_progressive,h_90,q_auto,w_90/https://dev-to-uploads.s3.amazonaws.com/uploads/user/profile_image/480052/f684c523-5316-4ac8-a73e-376d992dbcd4.jpeg",
            name: "Rohith V",
            date: "Mar 13",
          },
          title: "Graph Algorithm - Depth First Search",
          tags: [
            { text: "beginners", color: "green" },
            { text: "programming", color: "blue" },
            { text: "tutorial", color: "red" },
            { text: "career" },
          ],
          footer: {
            reactions: 8,
            comments: 5,
            time: 6,
          },
        },
        {
          author: {
            image:
              "https://res.cloudinary.com/practicaldev/image/fetch/s--bzrfhCEs--/c_fill,f_auto,fl_progressive,h_90,q_auto,w_90/https://dev-to-uploads.s3.amazonaws.com/uploads/user/profile_image/530414/941751d8-06b8-41bd-9de9-6ea056b7199f.png",
            name: "Tapajyoti Bose",
            date: "Mar 13",
          },
          title:
            "Automatically Format your code on Git Commit using Husky, ESLint, Prettier in 9 minutes",
          tags: [
            { text: "javascript", color: "yellow" },
            { text: "webdev", color: "purple" },
          ],
          footer: {
            reactions: 3,
            comments: 0,
            time: 5,
          },
        },
        {
          author: {
            image:
              "https://res.cloudinary.com/practicaldev/image/fetch/s--yG9NaJlu--/c_fill,f_auto,fl_progressive,h_90,q_auto,w_90/https://dev-to-uploads.s3.amazonaws.com/uploads/user/profile_image/161327/2ff05281-db58-4dcb-946a-4b679e4a266b.jpeg",
            name: "Alvaro Montoro",
            date: "Mar 13",
          },
          title: "Giving new meanings ot the color functions in CSS",
          tags: [
            { text: "parody", color: "green" },
            { text: "html", color: "blue" },
            { text: "css", color: "red" },
          ],
          footer: {
            reactions: 6,
            comments: 2,
            time: 3,
          },
        },
        {
          author: {
            image:
              "https://res.cloudinary.com/practicaldev/image/fetch/s--s2TtbFus--/c_fill,f_auto,fl_progressive,h_90,q_auto,w_90/https://dev-to-uploads.s3.amazonaws.com/uploads/user/profile_image/480052/f684c523-5316-4ac8-a73e-376d992dbcd4.jpeg",
            name: "Rohith V",
            date: "Mar 13",
          },
          title: "Graph Algorithm - Depth First Search",
          tags: [
            { text: "beginners", color: "green" },
            { text: "programming", color: "blue" },
            { text: "tutorial", color: "red" },
            { text: "career" },
          ],
          footer: {
            reactions: 8,
            comments: 5,
            time: 6,
          },
        },
      ],
    };
  },
};
</script>

<style></style>
