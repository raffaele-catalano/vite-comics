<script>
import { menuHeader } from '../data/db-menu';
export default {
    name: 'Header',
    data() {
        return {
            menuHeader
        }
    }
}
</script>

<template>
    <header>
        <div class="header-wrapper">
            <div class="logo-container">
                <img src="../assets/img/dc-logo.png" alt="dc-logo">
            </div>
            <div class="nav-container">
                <nav>
                    <ul>
                        <li v-for="(item, index) in menuHeader" :key="index">
                            <a :href="item.href">{{ item.label }}</a>
                        </li>
                    </ul>
                </nav>
            </div>
        </div>
    </header>
</template>

<style lang="scss" scoped>
@use '../scss/main.scss' as *;

header {
    display: flex;
    justify-content: center;
    height: 100px;
    width: 100%;
    background-color: $light;
    .header-wrapper {
        display: flex;
        justify-content: space-between;
        align-items: center;
        width: 65%;

        .logo-container {
            img {
                width: 80%;
            }
        }
        .nav-container {
            
            nav {
                ul {
                    li {
                        display: inline-block;
                        a {
                            color: $gray;
                            margin: 0 15px;
                            text-transform: uppercase;
                            font-size: $s-txt;
                            font-weight: $bold;
                            transition: all .3s;
                        }
                        a:hover {
                            color: $primary;
                            font-size: .9rem;
                        }
                    }
                }
            }
        }
    }
}
</style>