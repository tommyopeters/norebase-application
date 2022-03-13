<template>
  <aside class="right-sidebar">
    <Card classes="grey-card codeland">
      <div class="image-control">
        <img
          src="https://res.cloudinary.com/practicaldev/image/fetch/s--Su8MR3_z--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_350/https:/community.codenewbie.org/remoteimages/uploads/articles/nylmwmidrc3ugik4pgqr.png"
          alt=""
        />
      </div>
      <h3>CodeLand 2022: Taking place virtually on June 16 & 17</h3>
      <a href="">→ Learn More & Submit a talk</a>
    </Card>
    <Card classes="grey-card list-cards">
      <template v-slot:card-header>
        <h2>Listings</h2>
        <a href="">See all</a>
      </template>
      <template>
        <ul>
          <li>
            <p class="content">
              I Can Redesign Your Web Page / Site for Mobile Responsive
            </p>
            <div class="tag">forhire</div>
          </li>
          <li>
            <p class="content">
              How to create & publish our first NPM Package 😎 with 💖
            </p>
            <div class="tag">education</div>
          </li>
          <li>
            <p class="content">
              Inviting contributors 👩‍💻👨‍💻 to build Testsigma - Open Source
              Testing Tool! 🚀
            </p>
            <div class="tag">collabs</div>
          </li>
          <li>
            <p class="content">📝Live Resume Reviews</p>
            <div class="tag">events</div>
          </li>
          <li>
            <p class="content">
              📨 This Week In React: newsletter for professionals ⚛️
            </p>
            <div class="tag">collabs</div>
          </li>
        </ul>
      </template>
      <template v-slot:card-footer>
        Create a Listing
      </template>
    </Card>
    <Card classes="grey-card list-cards">
      <template v-slot:card-header>
        <h2>#help</h2>
      </template>
      <template>
        <ul>
          <li>
            <p class="content">
              Why I am unable to populate and select the custom item in juery-ui
              autocomoplete?
            </p>
            <div class="new">
              New
            </div>
          </li>
          <li>
            <p class="content">
              Printing Characters at a certain font size in go
            </p>
            <div class="new">New</div>
          </li>
          <li>
            <p class="content">
              React: Multiple projects inside of a react-app?
            </p>
            <div class="comments">2 comments</div>
          </li>
          <li>
            <p class="content">How do I customize my NeoVim setup in Linux?</p>
            <div class="comments">4 comments</div>
          </li>
          <li>
            <p class="content">
              Space Talks - ReactJs
            </p>
            <div class="new">New</div>
          </li>
        </ul>
      </template>
    </Card>
    <Card classes="grey-card list-cards">
      <template v-slot:card-header>
        <h2>#explainlikeimfive</h2>
      </template>
      <template>
        <ul>
          <li>
            <p class="content">
              What is meant by a "shape" in programming
            </p>
            <div class="new">
              New
            </div>
          </li>
          <li>
            <p class="content">
              Explain JavaScript promises Like I'm Five
            </p>
            <div class="new">New</div>
          </li>
          <li>
            <p class="content">
              Explain the difference between Front End developer & Back End
              Developer
            </p>
            <div class="comments">2 comments</div>
          </li>
          <li>
            <p class="content">
              Explain Dependency Injection (DI) like I am five.
            </p>
            <div class="comments">4 comments</div>
          </li>
          <li>
            <p class="content">
              Explain a "memory leak" like I'm five
            </p>
            <div class="new">New</div>
          </li>
        </ul>
      </template>
    </Card>
    <Card classes="grey-card list-cards">
      <template v-slot:card-header>
        <h2>#challenge</h2>
      </template>
      <template>
        <ul>
          <li>
            <p class="content">
              Why I am unable to populate and select the custom item in juery-ui
              autocomoplete?
            </p>
            <div class="new">
              New
            </div>
          </li>
          <li>
            <p class="content">
              Printing Characters at a certain font size in go
            </p>
            <div class="new">New</div>
          </li>
          <li>
            <p class="content">
              React: Multiple projects inside of a react-app?
            </p>
            <div class="comments">2 comments</div>
          </li>
          <li>
            <p class="content">How do I customize my NeoVim setup in Linux?</p>
            <div class="comments">4 comments</div>
          </li>
          <li>
            <p class="content">
              Space Talks - ReactJs
            </p>
            <div class="new">New</div>
          </li>
        </ul>
      </template>
    </Card>
    <Card classes="grey-card list-cards">
      <template v-slot:card-header>
        <h2>#meta</h2>
      </template>
      <template>
        <ul>
          <li>
            <p class="content">
              What is meant by a "shape" in programming
            </p>
            <div class="new">
              New
            </div>
          </li>
          <li>
            <p class="content">
              Explain JavaScript promises Like I'm Five
            </p>
            <div class="new">New</div>
          </li>
          <li>
            <p class="content">
              Explain the difference between Front End developer & Back End
              Developer
            </p>
            <div class="comments">2 comments</div>
          </li>
          <li>
            <p class="content">
              Explain Dependency Injection (DI) like I am five.
            </p>
            <div class="comments">4 comments</div>
          </li>
          <li>
            <p class="content">
              Explain a "memory leak" like I'm five
            </p>
            <div class="new">New</div>
          </li>
        </ul>
      </template>
    </Card>
  </aside>
</template>

<script>
import Card from "@/components/ui/Card";
export default {
  components: {
    Card,
  },
};
</script>

<style></style>
