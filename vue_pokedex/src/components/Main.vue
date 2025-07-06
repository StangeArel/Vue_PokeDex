<template>
    <main>
        <Card></Card>
        <Card></Card>
        <Card></Card>
        <Card></Card>
        <Card></Card>
        <Card></Card>
        <Card></Card>
        <Card></Card>
        <Card></Card>


    </main>
</template>

<script>
import Card from './Card.vue';

export default {
    components: {
        Card: Card
    }
}
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