<template>
  <div v-for="msg in messagesFiltered" :key="msg.id">
    {{ msg.text }}
  </div>
</template>

<script>
export default {
  data() {
    return {
      messages: [
        { id: 1, text: 'Hello', author: '1' },
        { id: 2, text: 'Hi', author: '2' },
        { id: 3, text: 'Bye', author: '3' },
        { id: 4, text: 'See you', author: '4' },
      ],
    }
  },
  computed: {
    messagesFiltered() {
      return this.messages.filter((msg) => {
        return `${msg.author}` === this.$route.params.chatId
      })
    },
  },
}
</script>
