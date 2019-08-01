<template>
  <div id="map"
       style="width:1200px;height:1000px;"></div>
</template>

<script>
import { data } from './data'
import * as d3 from 'd3'
import RelationChart from './index'
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  methods: {
    _init_() {
      var map = document.querySelector('#map')
      new RelationChart(map, data)
    }
  },
  mounted() {
    setTimeout(() => {
      this._init_()
    }, 110)
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
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
