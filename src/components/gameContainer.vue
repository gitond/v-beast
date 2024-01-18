<script setup>
    import gameScene from './gameScene.vue';
    import titleScene from './titleScene.vue';
    import { ref } from 'vue';

    let currentScene = ref(titleScene);

    function gs(){
        currentScene.value = gameScene;
    }
</script>

<template>
    <div class="gamecontainer">
        <component
            :is="currentScene"
            class="scene"
            @gameStart="gs"
        ></component>
    </div>
</template>

<style scoped></style>