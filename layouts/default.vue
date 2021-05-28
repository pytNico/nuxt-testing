<template>
  <div class="d-flex flex-column h-100">
    <n-header />
    <main class="container flex-shrink-0"><Nuxt /></main>
    <n-footer />
  </div>
</template>

<style>
html,
body,
#__nuxt,
#__layout {
  height: 100vh;
}

main.container {
  padding-top: 2em;
}

.page-enter-active,
.page-leave-active {
  transition: opacity 0.25s ease-in-out, transform 0.25s ease-in-out;
}
.page-enter,
.page-leave-to {
  opacity: 0;
  transform: translate3d(0, 15px, 0);
}
</style>
