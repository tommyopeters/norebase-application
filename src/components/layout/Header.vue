<template>
  <header>
    <div class="container">
      <div
        class="mobile-menu-trigger mobile-display"
        @click="emitMobileTrigger"
      >
        <svg
          xmlns="http://www.w3.org/2000/svg"
          width="24"
          height="24"
          viewBox="0 0 24 24"
          role="img"
          aria-labelledby="ae5egy0wb9hl8z52d1wnlikarltb0z18"
          class="crayons-icon"
        >
          <title id="ae5egy0wb9hl8z52d1wnlikarltb0z18">Navigation menu</title>
          <path d="M3 4h18v2H3V4zm0 7h18v2H3v-2zm0 7h18v2H3v-2z"></path>
        </svg>
      </div>
      <div class="logo image-control vertical">
        <img
          src="https://dev-to-uploads.s3.amazonaws.com/uploads/logos/resized_logo_UQww2soKuUsjaOGNB38o.png"
          alt=""
        />
      </div>
      <div class="search-box mobile-hide">
        <input type="text" placeholder="Search..." />
        <div class="btn search-btn">
          <svg
            xmlns="http://www.w3.org/2000/svg"
            width="24"
            height="24"
            viewBox="0 0 24 24"
            aria-hidden="true"
            class="crayons-icon c-btn__icon"
            focusable="false"
          >
            <path
              d="m18.031 16.617 4.283 4.282-1.415 1.415-4.282-4.283A8.96 8.96 0 0 1 11 20c-4.968 0-9-4.032-9-9s4.032-9 9-9 9 4.032 9 9a8.96 8.96 0 0 1-1.969 5.617zm-2.006-.742A6.977 6.977 0 0 0 18 11c0-3.868-3.133-7-7-7-3.868 0-7 3.132-7 7 0 3.867 3.132 7 7 7a6.977 6.977 0 0 0 4.875-1.975l.15-.15z"
            ></path>
          </svg>
        </div>
      </div>
      <div class="buttons">
        <div class="btn search-btn mobile-display">
          <svg
            xmlns="http://www.w3.org/2000/svg"
            width="24"
            height="24"
            viewBox="0 0 24 24"
            aria-hidden="true"
            class="crayons-icon c-btn__icon"
            focusable="false"
          >
            <path
              d="m18.031 16.617 4.283 4.282-1.415 1.415-4.282-4.283A8.96 8.96 0 0 1 11 20c-4.968 0-9-4.032-9-9s4.032-9 9-9 9 4.032 9 9a8.96 8.96 0 0 1-1.969 5.617zm-2.006-.742A6.977 6.977 0 0 0 18 11c0-3.868-3.133-7-7-7-3.868 0-7 3.132-7 7 0 3.867 3.132 7 7 7a6.977 6.977 0 0 0 4.875-1.975l.15-.15z"
            ></path>
          </svg>
        </div>
        <div class="btn btn-borderless btn-transparent mobile-hide">Log in</div>
        <div class="btn btn-blue">Create account</div>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  methods: {
    emitMobileTrigger: function() {
      this.$emit("mobile", true);
    },
  },
};
</script>

<style></style>
