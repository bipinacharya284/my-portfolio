<template>
  <div class="bg-gray-800 py-5 text-center text-white absolute bottom-0 w-full">
    <div class="flex flex-col">
      <span>
        Made with
        <Icon name="material-symbols:favorite-rounded" color="crimson" /> by
        Acharya Bipin(2023 -{{ date }})
      </span>
      <span sm:mt-3>
        <NuxtLink to="#">
          <Icon name="fa-brands:github" class="h-5 w-5 mr-2" />
        </NuxtLink>
        <NuxtLink to="#">
          <Icon name="fa-brands:facebook" class="h-5 w-5 mr-2" />
        </NuxtLink>
        <NuxtLink to="#">
          <Icon name="fa-brands:linkedin" class="h-5 w-5 mr-2" />
        </NuxtLink>
      </span>
    </div>
  </div>
</template>

<script setup>
const date = new Date().getFullYear();
</script>
