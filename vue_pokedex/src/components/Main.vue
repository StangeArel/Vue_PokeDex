<template>
    <main>
        <Card v-for="pokemon in pokemons" :name="pokemon.name"></Card>

        {{ pokemons }}

    </main>
</template>

<script setup>
import Card from './Card.vue';
import { ref } from 'vue';

const pokemons = ref([]);

fetch('https://pokeapi.co/api/v2/pokemon?limit=10&offset=0')
    .then(response => {
        if (!response.ok) {
            throw new Error('Network response was not ok');
        }
        return response.json();
    })
    .then(data => {
        // Hier wird die Datenverarbeitung durchgeführt
        pokemons.value = data.results;
    })
    .catch(error => {
        // Hier werden Fehler behandelt
        console.error('There has been a problem with your fetch operation:', error);
    });


</script>

<style scoped>
main {
    background-color: #77a3a3;
    height: 100%;
    padding: 16px;
    border-bottom-right-radius: 8px;
    border-bottom-left-radius: 8px;
    display: flex;
    gap: 10px;
    flex-wrap: wrap;
    align-items: center;
    justify-content: center;
}
</style>