<script>
import { menuCTA } from '../../data/db-menu';
export default {
    name: 'CTA',
    data() {
        return {
            menuCTA
        }
    }
}
</script>

<template>
    <div class="cta">
        <div class="container">
            <ul>
                <li v-for="(item, index) in menuCTA" :key="index">
                    <img :src="item.src" :alt="item.label">
                    <span>{{ item.label }}</span>
                </li>
            </ul>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use '../../scss/main.scss' as *;

.cta {
    width: 100%;
    height: 150px;
    background-color: $primary;
    margin-top: 25px;
    .container {
        display: flex;
        justify-content: center;
        height: 100%;
        width: 80%;
        margin: 0 auto;
        //debug
        // border: 3px solid crimson;
        ul {
            display: flex;
            align-items: center;
            justify-content: space-evenly;
            width: 100%;
            height: 100%;
            li {
                display: flex;
                align-items: center;
                gap: 15px;
                cursor: pointer;
                
                &:hover {
                    img{
                        transition: all .4s;
                        transform: scale(1.3);
                    }
                }
                
                img {
                    height: 50px;
                }
                &:last-child {
                    img{
                        width: 60px;
                    }
                }
                span {
                    color: $light;
                    text-transform: uppercase;
                    font-weight: $light-bold;
                }
            }
        }
    }
}
</style>