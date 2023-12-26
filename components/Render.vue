<template>

</template>

<script setup>
const props = defineProps({
  code: String
})
useHead({
  script: [props.code]
})

</script>
