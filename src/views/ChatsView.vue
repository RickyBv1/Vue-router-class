<template>
  <div>
    <aside>
      <div v-for="chat in chats" :key="chat.id">
        <RouterLink :to="`/chats/${chat.id}`">
          {{ chat.name }}
        </RouterLink>
      </div>
    </aside>
    <article>
      <RouterView />
    </article>
  </div>
</template>

<script>
import { RouterLink } from 'vue-router'

export default {
  data() {
    return {
      chats: [
        { id: 1, name: 'Ricky' },
        { id: 2, name: 'Joss' },
        { id: 3, name: 'Boris' },
        { id: 4, name: 'Gaby' },
      ],
    }
  },
}
</script>
