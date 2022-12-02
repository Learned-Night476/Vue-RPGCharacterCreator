<template>
    <div id="app">
        <button v-on:click="toggle='character-generator'">View All Characters </button>
        <button v-on:click="toggle='character-creator'">Create A Character </button>
        <CharacterGenerator v-show="toggle==='character-generator'"/> 
        <CharacterCreator v-show="toggle==='character-creator'" /> <!-- Tells Vue to toggle between the v-on: clicks-->
    </div>
</template>

<script>
    import CharacterGenerator from './components/CharacterGenerator.vue'
    import CharacterCreator from "./components/CharacterCreator.vue"
    export default {
        name: 'App',
        components: {
            CharacterGenerator,
            CharacterCreator
        },
        data: function(){
            return { // returns an object
                toggle: "character-generator" //Stores data locally on the application.
            }
        }
    }
</script>

<style>
    #app {
        font-family: Avenir, Helvetica, Arial, sans-serif;
        -webkit-font-smoothing: antialiased;
        -moz-osx-font-smoothing: grayscale;
        text-align: center;
        color: #2c3e50;
        margin-top: 60px;
        background-color: dodgerblue;
        color: black;
    }
</style>
