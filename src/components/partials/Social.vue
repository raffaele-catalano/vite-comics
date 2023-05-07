<script>
import { menuSocial } from '../../data/db-menu';
export default {
    name: 'Social',
    data() {
        return {
            menuSocial
        }
    }
}
</script>

<template>
    <div class="social-menu">
        <div class="container">

            <div class="sign-up-container">
                <h4>sign-up now!</h4>
            </div>

            <div class="social-container">
                <h3>follow us</h3>
                <ul>
                    <li v-for="(item, index) in menuSocial" :key="index">
                        <a href="item.href"><img :src="item.src" :alt="item.label"></a>
                    </li>
                </ul>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use '../../scss/main.scss' as *;

.social-menu {
    display: flex;
    justify-content: center;
    width: 100%;
    height: 100px;
    background-color: $social-gray;

    .container {
        display: flex;
        align-items: center;
        justify-content: space-between;
        width: 80%;
        height: 100%;
        //debug
        // border: 1px solid gold;

        .sign-up-container {
            display: flex;
            align-items: center;
            height: 100%;
            // width: 50%;
            h4 {
                color: $light;
                text-transform: uppercase;
                border: 2px solid $primary;
                padding: 10px;
            }
        }

        .social-container {
            display: flex;
            align-items: center;
            height: 100%;
            width: 50%;
            //debug
            // border: 1px solid limegreen;
            
            h3 {
                text-align: right;
                width: 70%;
                text-transform: uppercase;
                color: $primary;
            }
            ul {
                display: flex;
                align-items: center;
                justify-content: end;
                width: 30%;
                height: 100%;
                margin-left: 10px;
                //debug
                // border: 1px solid crimson;

                li {
                    padding: 0 5px;
                    transition: all .3s;

                    &:hover {
                        transform: scale(1.3);
                    }
                }
            }
        }
    }
}
</style>