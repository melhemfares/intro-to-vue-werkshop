<template>
  <!-- If you only want this to show once, get rid of the v-for-->
  <div v-for="i in 5">
    <ClickCounter />
  </div>
</template>

<script>
import ClickCounter from '@/components/ClickCounter.vue'

export default {
  components: {
    ClickCounter
  }
}
</script>

<style>

</style>
