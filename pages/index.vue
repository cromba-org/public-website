<script setup>
const menu = useState('menu', () => false)
</script>

<template>
  <div id="app">
    <MobileMenu v-if="menu" />
    <Introduction />
    <Lan />
    <AboutCromba />
    <Features />
    <EcoSystem />
    <DistributionPlan />
    <TimeLine />
    <JoinUs />
    <OurTeam />
    <Footer />
  </div>
</template>

<script>
export default {
  name: 'IndexPage',
}
</script>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Raleway:wght@400;600;700&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Roboto:wght@400;600;700&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Josefin+Sans:wght@400;600;700&display=swap');
body {
  margin: 0;
  padding: 0;
}
html {
  scroll-behavior: smooth;
}
#app {
  background-color: #11011e;
  overflow: hidden;
}
</style>
