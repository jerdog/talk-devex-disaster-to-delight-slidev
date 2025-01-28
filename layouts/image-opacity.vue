<script setup lang="ts">
import { computed } from 'vue'
import { handleBackground } from '../node_modules/@slidev/client/layoutHelper'

const props = defineProps({
  image: {
    type: String,
  },
  backgroundSize: {
    type: String,
    default: 'contain',
  },
  background: {
    type: String,
    default: 'rgba(0, 0, 0, 0.5)',
  },
})

const style = computed(() => handleBackground(props.image, false, props.backgroundSize))
</script>

<template>
  <div class="slidev-layout w-full h-full" :style="style + props.background">
    <slot />
  </div>
</template>
