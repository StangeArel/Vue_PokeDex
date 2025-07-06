<template>
    <header>
        <h1>PokeDex</h1>
        <input type="text" placeholder="Suche...">
    </header>
</template>

<script>
export default {
    name: 'Header',
}
</script>

<style scoped>
header {
    background-color: #f4bc39;
    height: 90px;
    padding: 16px;
    display: flex;
    align-items: flex-end;
    border-bottom-right-radius: 8px;
    border-bottom-left-radius: 8px;
    margin: 0;
}
</style>