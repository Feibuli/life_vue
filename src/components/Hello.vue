<template>
  <div class="hello">
    <h1 @click="change">{{ info }}</h1>
    <input type="text" v-model="info">
  </div>
</template>

<script>
export default {
  // http://www.cnblogs.com/gagag/p/6246493.html
  name: 'hello',
  data () {
    return {
      info: 'vue'
    }
  },
  methods: {
    change () {
      this.info = 'vue2'
    }
  },
  beforeCreate: function () {
    console.log('beforeCreate========>')
    console.log(this.info)
    console.log(this.$el)
  },
  created: function () {
    console.log('created========>')
    console.log(this.info)
    console.log(this.$el)
  },
  beforeMount: function () {
    console.log('beforeMount========>')
    console.log(this.info)
    console.log(this.$el)
  },
  mounted: function () {
    console.log('mounted========>')
    console.log(this.info)
    console.log(this.$el)
  },
  beforeUpdate: function () {
    console.log('beforeUpdate========>')
    console.log(this.info)
  },
  updated: function () {
    console.log('updated========>')
    console.log(this.info)
  },
  beforeDestroy: function () {
    console.log('beforeDestroy========>')
    console.log(this.info)
    console.log(this.$el)
  },
  destroyed: function () {
    console.log('destroyed========>')
    console.log(this.info)
    console.log(this.$el)
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
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
