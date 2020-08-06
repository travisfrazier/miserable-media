<template>
  <footer class="footer">
    <div class="container">
      <span v-html="settings.footer" />
      <div class="social-links">
        <a target="_blank" href="https://instagram.com/miserable.media"
          ><span>Instagram</span></a
        >
        <a target="_blank" href="https://www.youtube.com/c/TheMiserableCo/"
          ><span>YouTube</span></a
        >
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  data() {
    return {
      settings: require('../../data/theme.json'),
    };
  },
};
</script>

<style scoped>
.footer {
  font-size: 0.8rem;
  padding: 6rem 0;
}
.social-links span:first-of-type {
  margin-right: 10px;
}
</style>
