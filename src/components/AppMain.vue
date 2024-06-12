<template>
    <div class="container">
        <h1 class="text-center py-3">I miei progetti</h1>
    </div>
    <div class="container mt-5">
        <ul class="row g-4">
            <AppMainCard />
        </ul>
    </div>
</template>

<script>
import AppMainCard from './AppMain-card/AppMainCard.vue';


    export default {
        components: {
            AppMainCard
        },
        
        
    }
</script>

<style lang="scss" scoped>

</style>