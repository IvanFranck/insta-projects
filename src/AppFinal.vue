<script setup>
import {ref} from "vue"
import AppRating from './components/AppRating.vue';
import ThankYouState from './components/ThankYouState.vue';

const isRatingCardVissible = ref(true)
const note = ref()
const updateRatingCardVisibility = ({status, selectedNote}) => {
  note.value = selectedNote
  isRatingCardVissible.value = status
}

</script>

<template>
  <div class="container">
    <AppRating v-if="isRatingCardVissible" @submit="updateRatingCardVisibility"  />

    <Transition name="slide-fade" >
      <ThankYouState v-if="!isRatingCardVissible" :note="note"/>
    </Transition>
  </div>
</template>

<style lang="scss">
.slide-fade-enter-active {
  transition: all 0.3s ease-out;
}
.slide-fade-leave-active {
  transition: all 0.8s cubic-bezier(1, 0.5, 0.8, 1);
}

.slide-fade-enter-from{
  transform: translateX(20px);
  opacity: 0;
}

.container{
  min-height: 100vh;
  width: 100%;
  display: grid;
  justify-items: center;
  align-items: center;
  padding: 0 20px;
}
</style>