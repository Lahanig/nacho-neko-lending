<script setup>
import wiki from './MainComponents/WikiComponent.vue'
import slider from './MainComponents/SliderComponent.vue'
import trivia from './MainComponents/TriviaComponent.vue'
</script>

<template>
    <main>
        <wiki />
        <slider />
        <trivia />
    </main>
</template>

<style scoped>
main {
    display: block;
    position: relative;
}
</style>