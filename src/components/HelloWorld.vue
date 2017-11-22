<template>
<div class="hello">
  <h1>{{ count }}</h1>
  <h2 @click="add">click me</h2>
</div>
</template>

<script>
export default {
  name: 'HelloWorld',
  computed: {
    count() {
      return this.$store.state.count
    }
  },
  methods: {
    add() {
      this.$store.commit('increment')
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1,
h2 {
  font-weight: normal;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}
</style>
