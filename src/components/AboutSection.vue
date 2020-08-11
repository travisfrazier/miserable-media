<template>
  <section class="about">
    <div class="container about-container">
      <p>
        We are a digital media company based out of Northern Virginia that is
        passionate about storytelling. Our team consists of experienced and
        skilled videographers, photographers, audio engineers and design
        specialists. From the Amazon jungle to the Arctic circle, we have
        produced and published content all over the world.<br></br>
        
        We are passionate about creating documentaries, music videos, promotional content and 
        more. We would love to help you tell your story effectively and beautifully. <g-link to="/contact">Get in touch!</g-link>
      </p>
    </div>
  </section>
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
.about-container {
  padding: 0 1rem;
  p {
    font-size: 1em;
    font-weight: 400;
    line-height: 1.68;
    padding: 0;
    margin: 0;
    opacity: 0.6;
  }
}
</style>
