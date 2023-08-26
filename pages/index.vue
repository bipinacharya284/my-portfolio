<template>
  <Navbar />
  <Parallax :offset="scrollOffset"> </Parallax>

  <html class="scroll-smooth">
    <div
      class="bg-white px-10 scroll-mt-20 py-20 text-black scroll-smooth"
      id="about"
    >
      <h1 class="text-2xl pb-2 font-bold">Hey!</h1>
      <span class="text-2xl pb-1">I'm Acharya Bipin!</span> <br />
      <span class="text-2xl pb-1"
        >I am Passionate coder and nature photography enthusiast.</span
      >
      <br />
      <span class="text-2xl"
        >Feel free to get in touch with me or view my past works.</span
      >
    </div>
  </html>
  <div class="h-screen"></div>
  <!-- <Footer /> -->
</template>

<script>
export default {
  data() {
    return {
      scrollOffset: 0,
    };
  },
  methods: {
    updateScrollOffset() {
      this.scrollOffset = window.scrollY * 0.5;
    },
  },
  onmounted() {
    window.addEventListener("scroll", this.updateScrollOffset);
  },
  beforeUnmount() {
    window.removeEventListener("scroll", this.updateScrollOffset);
  },
};
</script>
