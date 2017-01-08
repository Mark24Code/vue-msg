<template>
    <div id="Bbox">
        <div>
            <p>来自store data：{{b_num}}</p>
            <p>来自store 本地 computed：{{b_store_num}}</p>
        </div>
        <div>
            <div>
                本地数据： {{s}}
                <input type="text" v-model="s">
            </div>
        </div>
    </div>
</template>
<script>
export default {
    name: 'Bbox',
    data() {
        return {
            b_num: this.$store.getters.count,
            s: ""
        }
    },
    computed: {
        b_store_num() {
            return this.$store.getters.count
        }
    },
    watch: {
        s: function() {
            console.log("B组件S在变化")
        },
        b_store_num: {
            handler: function() {
                console.log("B组件计算变量，正在变化，依赖vuex")
            },
            deep: true
        }
    },
    components: {}
}
</script>
<style>
</style>
