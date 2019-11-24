<template>
    <div class="count">
        <h1>This is a count page</h1>
        <!-- Get count data from Vuex store (state)-->
        {{$store.state.count}}
        <button @click="increment">+</button>
        <button @click="decrement">-</button>
    </div>
</template>

<script>
export default {
    methods: {
        increment() {
            this.$store.commit("increment");
        },
        decrement() {
            this.$store.commit("decrement");
        }
    }
}
</script>