<template>
  <div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    status: {
      type: String,
      required: false,
      validator: function (value) {
        return [
          'syncing',
          'synced',
          'version-conflict',
          'error'
        ].indexOf(value) !== -1
      }
    }
  },
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  },
  mounted() {
    // console.log(this.$_vk.tools.throttle)
  },
  computed: {
    todo() {
      return this.$store.getters.doneTodos
    }
  }
}
</script>

<style scoped>
h1, h2 {
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
