<template>
  <div>
    <right-slide-bar />
    <dash-board />
  </div>
</template>

<script>
import DashBoard from "../components/dashBoard.vue";
import rightSlideBar from "../components/rightSlideBar.vue";
export default {
  components: { rightSlideBar, DashBoard },
  name: "IndexPage",
};
</script>
