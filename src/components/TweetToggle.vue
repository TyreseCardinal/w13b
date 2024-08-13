<template>
  <div>
    <button @click="toggleView">Toggle View</button>
    <div v-if="isListView">
      <ul>
        <li v-for="tweet in tweets" :key="tweet.id">
          <strong>{{ tweet.user }}</strong>: {{ tweet.content }} <em>({{ tweet.dateCreated }})</em>
        </li>
      </ul>
    </div>
    <div v-else>
      <div class="card-view">
        <div v-for="tweet in tweets" :key="tweet.id" class="tweet-card">
          <strong>{{ tweet.user }}</strong>
          <p>{{ tweet.content }}</p>
          <em>{{ tweet.dateCreated }}</em>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isListView: true,
      tweets: [
        { id: 1, content: "Hello World!", user: "User1", dateCreated: "2024-08-13" },
        { id: 2, content: "Vue is awesome!", user: "User2", dateCreated: "2024-08-13" },
        { id: 3, content: "Vue is awesome!", user: "User3", dateCreated: "2024-08-13" },
        { id: 4, content: "Vue is awesome!", user: "User4", dateCreated: "2024-08-13" },
        { id: 5, content: "Vue is awesome!", user: "User5", dateCreated: "2024-08-13" },
        { id: 6, content: "Vue is awesome!", user: "User6", dateCreated: "2024-08-13" },
        { id: 7, content: "Vue is awesome!", user: "User7", dateCreated: "2024-08-13" },
      ]
    };
  },
  methods: {
    toggleView() {
      this.isListView = !this.isListView;
    }
  }
};
</script>

<style scoped>
.card-view {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
  gap: 1rem;
}

.tweet-card {
  border: 1px solid #ccc;
  padding: 1rem;
  border-radius: 4px;
  background-color: #f9f9f9;
}
</style>
