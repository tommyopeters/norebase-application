<template>
  <div class="mobile-menu">
    <div class="container">
      <div class="mobile-menu-header" @click="emitMobileTrigger">
        <h1>Dev Community</h1>
        <div class="mobile-menu-trigger">
          <svg
            xmlns="http://www.w3.org/2000/svg"
            width="24"
            height="24"
            viewBox="0 0 24 24"
            role="img"
            aria-labelledby="ae91eb7k7265adzvc89i925qj90nv98m"
            aria-hidden="true"
            class="crayons-icon c-btn__icon"
          >
            <title id="ae91eb7k7265adzvc89i925qj90nv98m">Close</title>
            <path
              d="M12 10.586l4.95-4.95 1.414 1.414-4.95 4.95 4.95 4.95-1.414 1.414-4.95-4.95-4.95 4.95-1.414-1.414 4.95-4.95-4.95-4.95L7.05 5.636l4.95 4.95z"
            ></path>
          </svg>
        </div>
      </div>
      <LeftSideBar :mobile="true"></LeftSideBar>
    </div>
  </div>
</template>

<script>
import LeftSideBar from "@/components/main/LeftSideBar";
export default {
  components: {
    LeftSideBar,
  },
  methods: {
    emitMobileTrigger: function() {
      this.$emit("mobile", true);
    },
  },
  mounted() {
    setTimeout(() => {
      let modal = document.querySelector(".mobile-menu .container");
      document.querySelector("body").addEventListener("click", (e) => {
        if (!modal.contains(e.target)) {
          this.emitMobileTrigger();
        }
      });
    }, 100);
  },
};
</script>

<style></style>
