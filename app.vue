<template>
  <div>
    <NuxtPage />
  </div>
</template>

<script>
export default {
    head: {
    link: [
      {
        rel: 'icon',
        href: '../assets/logo.svg',
      },
    ],
  },
  created() {
    document.title = 'Cromba is an open source social media for the free world'
  },
}
</script>
