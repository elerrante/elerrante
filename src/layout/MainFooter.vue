<template>
  <footer
    class="footer"
    :class="{ [`footer-${type}`]: type }"
    :data-background-color="backgroundColor"
  >
    <div class="container">
      
      <div class="copyright">
        &copy; {{ year }} <br> Made by myself with <md-icon>favorite</md-icon> using
        <a href="https://www.creative-tim.com/" target="_blank">Creative Tim</a>.
      </div>
    </div>
  </footer>
</template>
<script>
export default {
  props: {
    backgroundColor: String,
    type: String
  },
  data() {
    return {
      year: new Date().getFullYear()
    };
  }
};
</script>
<style></style>
