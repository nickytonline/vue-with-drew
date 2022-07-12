<template>
  <div class="flex flex-col">
    <header>
      <h1>{{ greeting }}</h1>
    </header>

    <button type="button" class="bg-gray-200 p-2" @click="increment">
      Increment
    </button>
    <CounterDisplay :counter="counter">{{ doubleCount }}</CounterDisplay>
    <CounterDisplay2>
      <template slot="counter1">{{ counter }}</template>
      <template slot="counter2">{{ doubleCount }}</template>
    </CounterDisplay2>
    <label
      >Change greeting
      <input v-model="greeting" type="text" class="bg-gray-200" />
    </label>
    <ul>
      <li v-for="post in posts" :key="post.id">{{ post.title }}</li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'IndexPage',
  data() {
    return {
      greeting: 'Hello Vue!',
      counter: 0,
      posts: [
        { id: 1, title: 'Hello World' },
        { id: 2, title: 'Second Post' },
        { id: 3, title: 'Third Post' },
      ],
    }
  },
  computed: {
    doubleCount() {
      // Always has to return something or errors out
      return this.counter * 2
    },
  },
  methods: {
    increment() {
      this.counter++
    },
  },
}
</script>
