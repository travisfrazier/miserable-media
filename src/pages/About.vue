<template>
  <Layout>
    <div class="container">
      <Hero />
      <AboutSection />
    </div>
    <!-- <LatestBlogs :blogs="$page.blogs.edges" /> -->
  </Layout>
</template>

<script>
import Hero from "@/components/Hero"
import AboutSection from "@/components/AboutSection"


export default {
  components: {
    Hero,
    AboutSection  }
}
</script>
