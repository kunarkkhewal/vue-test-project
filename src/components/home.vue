<template>
  <div>
    <div class="bg-green-200 border rounded-lg">Home Page</div>
    <p>{{ $store.state.count }}</p>
    <button class="border rounded-sm mt-2 px-2" @click="increment">increment</button>
    <p>done todo count - {{doneTodosCount}}</p>
  </div>
</template>

<script>
// import store from '@/store'
export default {
  name: 'home-page',
  // store,
  methods: {
    increment () {
      console.log(' ------- in here')
      this.$store.commit('increment');
    }
  },
  computed: {
    doneTodosCount () {
      return this.$store.getters.doneTodos.length
    }
  }
}
</script>