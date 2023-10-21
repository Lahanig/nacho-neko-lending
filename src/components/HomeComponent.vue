<script setup>
import wiki from './MainComponents/WikiComponent.vue'
import slider from './MainComponents/SliderComponent.vue'
import trivia from './MainComponents/TriviaComponent.vue'
import FooterComponent from './MainComponents/FooterComponent.vue'
</script>

<template>
    <main>
        <a name="name-card"></a>
        <wiki />
        <a name="gallery"></a>
        <slider />
        <a name="trivia"></a>
        <trivia />
        <footer-component />
    </main>
</template>

<style scoped>
main {
    display: block;
    position: relative;
}
</style>