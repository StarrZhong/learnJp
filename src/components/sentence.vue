<script setup>

import { ref, computed } from 'vue'
import gojuonHelper from './../helpers/gojuon'
const props = defineProps({
  msg: String,
})

let songWords = computed(()=>{
    return props.msg
})

</script>

<template>
    <p>
        <span class="sentence">
            <ruby>
            <rb>{{ songWords }}</rb>
            <rt>
                <ruby v-for="(sItem,index) in gojuonHelper.transfer(songWords)">
                <rb>{{ sItem.text }}</rb>
                <rt class="en">{{sItem.alphabetical}}</rt>
                </ruby>
            </rt>
            </ruby>
            
            
        </span>
        
  </p>
</template>

<style scoped>

</style>
