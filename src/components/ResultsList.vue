<template>
    <div>
        <h2>Pokemon</h2>
        <ul>
            <Pokemon
                v-for="result in pokemon"
                :key="result.url"
                :result="result"
            />
        </ul>
    </div>
</template>

<script>
import Pokemon from './Pokemon'

export default {
    props: ['pokemon'],
    components: {
        Pokemon
    }
}
</script>

<style>

</style>
