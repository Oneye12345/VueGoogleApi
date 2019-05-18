<template>
  <div id="app" class="container">
    <myMap />
  </div>
</template>

<script>
//console.log("App called");
import myMap from './components/my-map.vue'
export default {
  name: 'app',
  data () {
    return {
    }
    
  },
  components: {
    myMap
  }
}
</script>

<style>

</style>
