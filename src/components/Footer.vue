<template>
  <footer class="footer">
    <div class="container footer-container">
      <span class="social-links">
        <a
          class="instagram"
          target="_blank"
          href="https://instagram.com/miserable.media"
          ><font-awesome class="social-icon" :icon="['fab', 'instagram']"
        /></a>
        <a target="_blank" href="https://www.youtube.com/c/TheMiserableCo/"
          ><font-awesome class="social-icon" :icon="['fab', 'youtube']"
        /></a>
        <a target="_blank" href="https://twitter.com/themiserableco"
          ><font-awesome class="social-icon" :icon="['fab', 'twitter']"
        /></a>
      </span>
      <span v-html="settings.footer" />
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

<style scoped lang="scss">
.footer {
  margin-top: 3rem;
  font-size: 0.8rem;
  padding: 6rem 0;
  background-color: #d9bc7a;
}
.footer-container {
  display: flex;
  justify-content: center;
  flex-direction: column;
  align-items: center;
}
.social-links {
  font-size: 1.5rem;
  margin-bottom: 0.5rem;
  a {
    padding: 0.74rem;
  }
}
</style>
