<script setup>
const games = [331670, 397460, 434170, 610180, 774461, 1005300, 1211630, 1552350, 1850960, 2216830]
const useImage = ((url) => {
  return new URL(`/src/assets/${url}`, import.meta.url).href;
});
</script>

<template>
    <div class="row">
        <div
            class="col-md-4 mb-4"
            v-for="game in games"
        >
            <a
                :href="`steam://rungameid/${game}`">
                <img
                    class="expand-on-hover mw-100"
                    :src="useImage(`party_pack_${games.indexOf(game) + 1}.jpg`)"
                    :alt="`Party Pack ${games.indexOf(game) + 1}`"
                >
            </a>
        </div>
    </div>
</template>

<style lang="scss" scoped>
.expand-on-hover {
    transition: all .25s ease-in-out;

    &:hover {
        transform: scale(1.1);
    }
}
</style>
