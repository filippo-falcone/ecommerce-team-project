<script>
import AppHeader from './components/AppHeader.vue';
import Discover from './components/Discover.vue';

export default {
    components: {
        AppHeader,
        Discover
    }
}
</script>

<template>
    <AppHeader></AppHeader>
    <main>
        <Discover></Discover>
    </main>
</template>

<style lang="scss">
@use './style/generic.scss';
</style>