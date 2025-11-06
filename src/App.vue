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