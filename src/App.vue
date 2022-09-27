<script setup>
import GameList from './components/GameList.vue'
</script>

<template>
    <div class="container mt-4">
        <div class="text-center">
            <img
                width="750"
                height="250"
                class="text-center mw-100"
                alt="Jackbox Logo"
                src="./assets/logo.png"
            />
        </div>
        <hr />
        <GameList />
    </div>
</template>
