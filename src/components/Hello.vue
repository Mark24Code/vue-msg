<template>
    <div class="hello">
        <div class="Hcont">
            <p>本地属性：{{hname}}</p>
            <p>data=store.count:{{store_num}}</p>
            <p>comp=store.count:{{store_com_num}}</p>
        </div>
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
    data() {
        return {
            hname: 'This is hello',
            store_num: this.$store.getters.count
        }
    },
    computed:{
      store_com_num(){
        return this.$store.getters.count
      }
    },
    components: {
        Abox,
        Bbox
    }
}
</script>
<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.Acont,
.Bcont,
.Hcont {
    height: 150px;
    width: 100%;
    margin: 10px;
    border: 1px solid #000;
}
</style>
