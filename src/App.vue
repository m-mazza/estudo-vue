<script setup>
    import TheHeader from './components/TheHeader.vue';
    import TodoList from './components/TodoList.vue';
    import TheFooter from './components/TheFooter.vue';
</script>

<template>
    <div id="app-wrapper">
        <div class="container">
            <TheHeader/>
            <main>
            <TodoList/>
            </main>
            <TheFooter/>
        </div>
    </div>
</template>

<style scoped>

    /* ao atribuir o atributo 'scoped' na tag style, a estilização criada pertence somente ao compnente a esse componente. Como ele faz isso? o Vue cria um atributo aleatório junto a classe especificada aqui no componete, tornado - de certa forma - essa classe, única. */
    #app-wrapper {
        border: 1px solid blue;
        height: 100vh;
        display: flex;
        justify-content: center;
        align-items: center;
    }
    .container {
        width: 1080px;
    }
</style>