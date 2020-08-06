<template>
  <footer class="footer">
    <div class="container footer-container">
      <span v-html="settings.footer" />
      <span class="social-links">
        <a
          class="instagram"
          target="_blank"
          href="https://instagram.com/miserable.media"
          ><span>Instagram</span></a
        >
        <a target="_blank" href="https://www.youtube.com/c/TheMiserableCo/"
          ><span>YouTube</span></a
        >
      </span>
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
  margin-top: 3rem;
  font-size: 0.8rem;
  padding: 6rem 0;
  background-color: #d9bc7a;
}
span {
  padding: 1rem;
}
@media only screen and (max-width: 768px) {
  .footer-container {
    display: grid;
  }
  span {
    padding: 0;
  }
  .instagram {
    margin-right: 1rem;
  }
}
</style>
