<template>
    <div class="character-creator">
        <h1>Character Creator</h1>
        <label for="character-name">Character Name: </label>
        <input type="text" id="character-name" v-model="name" placeholder="Enter a character name" /><br /><br /> <!-- breaks added-->
        <label for="character-class-list">Character Class</label>

        <select id="character-class-list" v-model="occupation">
            <option value="Warrior">Warrior</option>
            <option value="Wizard">Wizard</option>
            <option value="Rogue">Rogue</option>
            <option value="Adventurer">Adventurer</option>
            <option value="Mage">Mage</option>

        </select>
        <label for="charater-weapon-choice">Weapon Choice</label>
          <select id="character-weapon-choice" v-model="weapons">
              <option value="Long Sword">Long Sword</option>
              
          </select>
        <p> {{ name }} </p>
        <p> {{ occupation }} </p>
        <p> {{ weapons }} </p>
    </div> <!-- v-model links data to the name-->
</template>

<script>
    export default {
        name: 'CharacterCreator',
        data: function () { // Added the data function which returns an object.
            return {
                name: "", //input is pointing to this variable in the data object.
                occupation: "",
                weapons: ""
      
            }
        }
    }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
    h3 {
        margin: 40px 0 0;
    }

    ul {
        list-style-type: none;
        padding: 0;
    }

    li {
        display: inline-block;
        margin: 0 10px;
    }

    a {
        color: #42b983;
    }
</style>
