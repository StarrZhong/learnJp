<script setup>
    import songData from './songData/sekai.json'
    import Sentence from "./components/sentence.vue";
    console.log(songData)
    import { ref } from 'vue'

    const currentSong = ref(songData);
</script>

<template>
  <Sentence v-for="(item,index) in currentSong" :msg="item"></Sentence>
  
</template>

<style scoped>

</style>
