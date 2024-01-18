<script setup>
    import gameScene from './gameScene.vue';
    import titleScene from './titleScene.vue';
    import { ref } from 'vue';

    let currentScene = ref('title');

    function gs(){
        console.log(currentScene);
        currentScene.value = 'game';
        console.log(currentScene);
    }
</script>

<template>
    <div class="gamecontainer">
        <titleScene 
            v-if="currentScene === 'title'"
            @gameStart="gs"
        />
        <gameScene />
    </div>
</template>

<style scoped></style>