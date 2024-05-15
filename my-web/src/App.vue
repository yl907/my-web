<script setup>
  import TextRendering from './components/1TextRendering.vue'
  import Flex1 from './components/2_1Flex.vue'
  import Flex2 from './components/2_2Flex.vue'
  import Grid1 from './components/3_1Grid.vue'
  import Grid2 from './components/3_2Grid.vue'
  import Grid3 from './components/3_3Grid.vue'
  import Grid4 from './components/3_4Grid.vue'
  import Float1 from './components/4_1Float.vue'
  import Float2 from './components/4_2Float.vue'
  import Float3 from './components/4_3Float.vue'
</script>

<template>
  <TextRendering></TextRendering>
  <hr />
  <Flex1></Flex1>
  <hr />
  <Flex2></Flex2>
  <hr />
  <Grid1></Grid1>
  <hr />
  <Grid2></Grid2>
  <hr />
  <Grid3></Grid3>
  <hr />
  <Grid4></Grid4>
  <hr />
  <Float1></Float1>
  <hr />
  <Float2></Float2>
  <hr />
  <Float3></Float3>
  <hr />
</template>

<style scoped>
  hr {
    --margin-top-and-bottom: 1em;
    margin-top: var(--margin-top-and-bottom);
    margin-bottom: var(--margin-top-and-bottom);
  }
  
</style>
