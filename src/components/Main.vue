<script>
import Card from './partials/Card.vue'
export default {
    name: 'Main',
    components: {
        Card,
    }
}
</script>

<template>
    <main>
        <div class="main-wrapper">
            <div class="container">
                <h4>Current Series</h4>
                <div class="cards-container">
                    <Card />
                </div>
                <button>Load More</button>
            </div>
        </div>
    </main>
</template>

<style lang="scss" scoped>
@use '../scss/main.scss' as *;

main {
    .main-wrapper {
        display: flex;
        flex-direction: column;
        position: relative;
        margin: 0 auto;
        width: 90%;
        text-align: center;
        // debug
        color: white;
        .cards-container{
            display: flex;
            flex-wrap: wrap;
            width: 100%;
            // .card {
            //     width: calc(100% / 6 - 20px);
            //     padding: 0 10px;
            //     margin: 10px;
            //     //debug
            //     border: 1px solid $primary;
            //     height: 100px;
            // }
        }
        button {
            padding: 10px 35px;
            background-color: $primary;
            border: none;
            color: $light;
            text-transform: uppercase;
            font-weight: $bold;
            cursor: pointer;
        }
    }
}
</style>