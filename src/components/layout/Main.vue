<template>
  <main>
    <div class="container">
      <LeftSideBar></LeftSideBar>
      <MainContent></MainContent>
      <RightSideBar></RightSideBar>
    </div>
  </main>
</template>

<script>
import MainContent from "@/components/main/MainContent";
import LeftSideBar from "@/components/main/LeftSideBar";
import RightSideBar from "@/components/main/RightSideBar";

export default {
  components: {
    MainContent,
    LeftSideBar,
    RightSideBar,
  },
};
</script>

<style></style>
