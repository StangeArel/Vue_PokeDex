<template>
    <div class="pokeCard">
        <p>{{ name }}</p>
    </div>
</template>

<script setup>

defineProps(['name'])

</script>

<style scoped>
.pokeCard {
    background-color: #d573d0;
    height: 20%;
    width: 20%;
    border-radius: 10px;
}
</style>