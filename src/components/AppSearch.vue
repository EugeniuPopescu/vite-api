<script>
import { store } from "../store.js"


export default {
	name: 'AppSearch',
	data() {
        return {
            store
        }
    },
    methods: {
        search() {
            console.log('Search: ', this.store.searchString);
            // avvisa il padre
            this.$emit('search')
        },
    },
    mounted() {}
}
</script>

<template>
    <div>
        <input placeholder="Cerca..." v-model="store.searchString" @keyup.enter="$emit('search')">
        <button @click="search">Cerca</button>
    </div>
</template>

<style scoped>

</style>