<template>
  <div class="hello">
    <div class="Hcont">{{hname}}</div>
    <div class="Acont">
    <p>Acont</p>
      <Abox></Abox>
    </div>
    <div class="Bcont">
    <p>Bcont</p>
      <Bbox></Bbox>
    </div>

  </div>
</template>

<script>
import Abox from './Abox.vue'
import Bbox from './Bbox.vue'

export default {
  name: 'hello',
  data () {
    return {
      hname:'This is hello'
    }
  },
  components:{
    Abox,
    Bbox
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.Acont,.Bcont,.Hcont{
  height: 100px;
  width: 100%;
  margin: 10px;
  border: 1px solid #000;
}
</style>
