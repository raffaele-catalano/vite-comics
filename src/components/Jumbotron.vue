<script>
export default {
    name: 'Jumbotron',
}
</script>

<template>
    <div class="jumbotron">
        <img src="../assets/img/jumbotron.jpg" alt="jumbotron_image">
    </div>
</template>

<style lang="scss" scoped>
@use '../scss/main.scss' as *;

.jumbotron {
    height: 400px;
    overflow: hidden;
}
</style>