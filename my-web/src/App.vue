<script setup>
  import TextRendering from './components/1TextRendering.vue'
  import Flex1 from './components/2_1Flex.vue'
  import Flex2 from './components/2_2Flex.vue'
</script>

<template>
  <TextRendering></TextRendering>
  <hr />
  <Flex1></Flex1>
  <hr />
  <Flex2></Flex2>
  <hr />
</template>

<style scoped>
  hr {
    --margin-top-and-bottom: 1em;
    margin-top: var(--margin-top-and-bottom);
    margin-bottom: var(--margin-top-and-bottom);
  }
  
</style>
