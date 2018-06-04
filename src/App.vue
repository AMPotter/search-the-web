<template>
  <div>
    <SearchControl :onSearch="handleSearch"/>
    <ResultsList :pokemon="pokemon"/>
  </div>
</template>

<script>
import ResultsList from './components/ResultsList';
import SearchControl from './components/SearchControl';
import { getPokemon } from './services/api.js'

export default {
  data() {
    return {
      pokemon: null
    };
  },
  components: {
    ResultsList,
    SearchControl
  },
  methods: {
    handleSearch(name) {
      getPokemon(name).then(data => {
        this.pokemon = data;
      });
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
