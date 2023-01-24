<template>
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