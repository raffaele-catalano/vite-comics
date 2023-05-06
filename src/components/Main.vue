<script>
import Card from './partials/Card.vue'
import CTA from './partials/CTA.vue'
import ComicsJson from '../data/dc-comics.json'
export default {
    name: 'Main',
    components: {
        Card,
        CTA
    },
    data () {
        return {
            ComicsJson,
        }
    }
}
</script>

<template>
    <main>
        <div class="main-wrapper">
            <div class="container">
                <h4>Current Series</h4>
                <div class="cards-container">
                    <Card v-for="(comic, index) in ComicsJson" :key="index" :Thumb="comic.thumb" :Series="comic.series" :Type="comic.type" :Price="comic.price"/>
                </div>
                <button>Load More</button>
            </div>
        </div>
        <CTA />
    </main>
</template>

<style lang="scss" scoped>
@use '../scss/main.scss' as *;

main {
    margin: 40px 0;
    .main-wrapper {
        display: flex;
        flex-direction: column;
        position: relative;
        margin: 0 auto;
        width: 80%;
        text-align: center;
        .container {
            h4 {
                background-color: $primary;
                max-width: 200px;
                color: $light;
                text-transform: uppercase;
                padding: 15px;
                position: absolute;
                top: -70px;
            }
            .cards-container{
                display: flex;
                flex-wrap: wrap;
                width: 100%;
                margin-bottom: 25px;
            }
            button {
                padding: 10px 35px;
                background-color: $primary;
                border: none;
                color: $light;
                text-transform: uppercase;
                cursor: pointer;
                font-weight: $bold;
            }
        }
    }
}
</style>