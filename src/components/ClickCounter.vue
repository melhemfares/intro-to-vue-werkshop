<template>
  <div class="container">
    <h1> {{ name }}'s Click Counter </h1>
  </div>

  <div class="display">
    <h3> You have clicked {{ clicks }} times </h3>
  </div>

  <div class="buttons">
    <button @click="increaseCount"> Click me! </button>
    <button @click="resetClicks"> Reset </button>
    <button @click="toggleVisibility"> Change name </button>
  </div>

  <div class="form">
    <input v-show="visibility" v-model="name"/>
  </div>
</template>

<script>
export default {
  data() {
    return {
      clicks: 0,
      name: 'Melly',
      visibility: true
    }
  },
  methods: {
    increaseCount() {
      this.clicks += 1;
    },
    toggleVisibility() {
      this.visibility = !this.visibility
    },
    resetClicks() {
      this.clicks = 0
    }
  }
}
</script>

<style scoped>
  .container {
    margin: auto;
    width: 100%
  }

  .buttons {
    display: flex;
    justify-content: center;
    flex-direction: column;
    margin: auto;
    width: 125px;
  }

  button {
    margin: 5px;
    padding: 8px;
  }

  .form {
    margin: 20px;
  }
</style>