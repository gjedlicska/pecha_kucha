<script setup lang="ts">
import { computed } from 'vue'
import { handleBackground } from '../layoutHelper'
const props = defineProps({
  image: {
    type: String,
  },
  cover: {
    type: Boolean
  }
})
const style = computed(() => handleBackground(props.image, false, props.cover))
console.log(props.cover, style)
</script>

<template>
  <div class="bg-black slidev-layout w-full h-full intro-image" :style="style">
    <slot />
  </div>
</template>