<template>
    <form @submit.prevent="onSearch(search)">
        <label>Pokemon Name:</label>
        <input v-model="search" />
        <button type="submit">Search</button>
    </form>
</template>

<script>
export default {
    data() {
        return { search: '' }
    },
    props: {
        onSearch: {
            type: Function,
            required: true
        }
    }
}
</script>

<style>

</style>
