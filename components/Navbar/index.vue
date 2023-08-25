<template>
  <!-- from-transparent -->
  <nav class="bg-gradient-to-r from-black to-transparent z-20 sticky top-0">
    <div
      class="max-w-7xl px-4 sm:px-6 lg:px-8 transition-all ease-in-out delay-300"
    >
      <div
        class="flex items-center justify-between h-1/2 py-6 transition-all ease-in-out delay-300"
      >
        <div class="flex items-center">
          <div class="flex-shrink-0 text-2xl text-white">Acharya Bipin</div>
        </div>
        <div class="hidden md:flex space-x-4 absolute right-10">
          <a
            href="#about"
            class="text-gray-400 text-xl transition ease-in-out duration-300 hover:text-white scroll-smooth"
            >About Me</a
          >
          <a
            href="#"
            class="text-gray-400 text-xl transition ease-in-out duration-300 hover:text-white"
            >Portfolio</a
          >
          <a
            href="#"
            class="text-gray-400 text-xl transition ease-in-out duration-300 hover:text-white"
            >Never Ending List
          </a>
        </div>
        <div class="flex flex-col">
          <div class="md:hidden">
            <!-- transition transform hover:-translate-y-1 motion-reduce:transition-none motion-reduce:hover:transform-none ..." -->
            <button class="text-white" @click="toggleMobileMenu">
              <Icon v-if="!isMobileMenuActivate" name="bi:list" />
              <Icon v-else name="bi:x-lg" />
            </button>
          </div>
          <div v-if="isMobileMenuActivate" class="md:hidden h-auto">
            <div class="flex flex-col bg-grey-800">
              <a href="#" class="text-gray-300 hover:text-white py-2"
                >About Me</a
              >
              <a href="#" class="text-gray-300 hover:text-white py-2"
                >Portfolio</a
              >
              <a href="#" class="text-gray-300 hover:text-white py-2"
                >Never Ending List</a
              >
            </div>
          </div>
        </div>
      </div>
    </div>
    <!-- You can add other components here -->
  </nav>
</template>

<script>
// import smoothScroll from 'plugins/smooth-scroll';
export default {
  data() {
    return {
      isMobileMenuActivate: false,
    };
  },
  methods: {
    toggleMobileMenu() {
      this.isMobileMenuActivate = !this.isMobileMenuActivate;
    },
  },
};
</script>

<style>
template {
  scroll-behavior: smooth;
}
</style>
