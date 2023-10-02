<script setup>
import AppRating from './components/AppRating.vue';
import ThankYouState from './components/ThankYouState.vue';

</script>

<template>
  <div class="container">
    <AppRating/>
    <ThankYouState/>
  </div>
</template>

<style lang="scss" scoped>
.container{
  min-height: 100vh;
  width: 100%;
  display: grid;
  justify-items: center;
  align-items: center;
  padding: 0 20px;
}
</style>