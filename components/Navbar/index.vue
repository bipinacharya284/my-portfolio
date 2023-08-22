<template>
  <nav class="bg-gray-800">
    <div class="max-w-7xl px-4 sm:px-6 lg:px-8 transition-all ease-in-out delay-300">
      <div class="flex items-center justify-between h-1/2 py-6 transition-all ease-in-out delay-300">
        <div class="flex items-center">
          <div class="flex-shrink-0 text-white">Logo</div>
        </div>
        <div class="hidden md:flex space-x-4 absolute right-10">
          <a href="#" class="text-gray-300 text-xl hover:text-white">About Me</a>
          <a href="#" class="text-gray-300 text-xl hover:text-white">Portfolio</a>
          <a href="#" class="text-gray-300 text-xl hover:text-white">Never Ending List </a>
        </div>
        <div class="flex flex-col">
          <div class="md:hidden">
            <button class="text-white" @click="toggleMobileMenu">
              <Icon v-if="!isMobileMenuActivate" name="bi:list" />
              <Icon v-else name="bi:x-lg" />
            </button>
          </div>
          <div v-if="isMobileMenuActivate" class="md:hidden h-auto">
            <div class="flex flex-col bg-grey-800">
              <a href="#" class="text-gray-300 hover:text-white py-2">About Me</a>
              <a href="#" class="text-gray-300 hover:text-white py-2">Portfolio</a>
              <a href="#" class="text-gray-300 hover:text-white py-2">Never Ending List</a>
            </div>
          </div>
        </div>
      </div>
    </div>
    <!-- You can add other components here -->
  </nav>
</template>

<script>
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
