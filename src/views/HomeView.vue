<script>
export default {
  data() {
    return {
      username: '',
    }
  },
}
</script>

<template>
  <main>
    <h3>Introduce your username</h3>
    <input placeholder="username" v-model="username" />
  </main>
</template>
