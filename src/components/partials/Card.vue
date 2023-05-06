<script>
export default {
    name: 'Card',
}
</script>

<template>
    
    <div class="card">

        <div class="image-container">
            <p>IMG</p>
        </div>
        
        <div class="txt-container">
            <span>TITLE</span>
        </div>

    </div>

</template>

<style lang="scss" scoped>
@use '../../scss/main.scss' as *;
.card {
    width: calc(100% / 6 - 20px);
    padding: 0 10px;
    margin: 10px;
    // debug
    border: 1px solid $primary;
    height: 100px;
}
</style>