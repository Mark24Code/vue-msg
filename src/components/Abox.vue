<template>
    <div id="Abox">
        <div>
            {{a_num}}<input type="text" v-model="a_num">
        </div>
        <div>
            <button @click="trans">通信</button>
        </div>
    </div>
</template>
<script>
export default {
    name: 'Abox',
    data() {
        return {
            a_num: 0
        }
    },
    methods: {
        trans() {
            console.log("A组件Trans按下");
            this.$store.dispatch("inc")
        }
    }
}
</script>
<style>
</style>
