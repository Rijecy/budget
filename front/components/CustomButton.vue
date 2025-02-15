<template>
  <div class="">
    <button :class="colorClass" class="px-4 py-2 shadow-2xl rounded-2xl1">{{ label }}</button>
  </div>
</template>

<script setup lang="js">
const props = defineProps(['label', 'color'])

const colorClass = computed(() => {
  switch (props.color) {
    case 'blue': return 'bg-blue-600'
    case 'red': return 'bg-red-600'
    case 'orange': return 'bg-orange-600'
    case 'green': return 'bg-green-600'
    default: return 'bg-white'
  }
  })
</script>