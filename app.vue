<template>
  <NuxtLayout>
    <Transition
      name="page"
      mode="out-in"
      appear
      enter-active-class="transition-all duration-350 ease-[cubic-bezier(0.4,0,0.2,1)]"
      enter-from-class="opacity-0 scale-95 blur-sm"
      enter-to-class="opacity-100 scale-100 blur-0"
      leave-active-class="transition-all duration-150 ease-[cubic-bezier(0.4,0,0.2,1)]"
      leave-from-class="opacity-100 scale-100 blur-0"
      leave-to-class="opacity-0 scale-95 blur-sm"
    >
      <NuxtPage />
    </Transition>
  </NuxtLayout>
</template>
<script setup>
useHead({
  script: [
    { src: "https://identity.netlify.com/v1/netlify-identity-widget.js" },
  ],
});
</script>
