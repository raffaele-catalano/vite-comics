<script>
export default {
    name: 'Footer',
}
</script>

<template>
    <footer>
        <div class="container">

            <div class="footer-nav">
                <!-- first column -->
                <div class="col">

                    <ul>
                        <h4>dc comics</h4>
                        <li>
                            <a href="#">characters</a>
                            <a href="#">comics</a>
                            <a href="#">movies</a>
                            <a href="#">TV</a>
                            <a href="#">games</a>
                            <a href="#">video</a>
                            <a href="#">news</a>
                        </li>
                    </ul>

                    <ul>
                        <h4>shop</h4>
                        <li>
                            <a href="#">shop DC</a>
                            <a href="#">shop DC collectibles</a>
                        </li>
                    </ul>

                </div>
                <!-- second column -->
                <div class="col">
                    <ul>
                        <h4>dc</h4>
                        <li>
                            <a href="#">terms of use</a>
                            <a href="#">privacy policy</a>
                            <a href="#">ad choices</a>
                            <a href="#">advertising</a>
                            <a href="#">jobs</a>
                            <a href="#">subscriptions</a>
                            <a href="#">talent workship</a>
                            <a href="#">CSPC certificates</a>
                            <a href="#">ratings</a>
                            <a href="#">shop help</a>
                            <a href="#">contact us</a>
                        </li>
                    </ul>
                </div>
                <!-- third column -->
                <div class="col">
                    <ul>
                        <h4>sites</h4>
                        <li>
                            <a href="#">DC</a>
                            <a href="#">MAD magazine</a>
                            <a href="#">DC kids</a>
                            <a href="#">DC universe</a>
                            <a href="#">DC power visa</a>
                        </li>
                    </ul>
                </div>
            </div>

            <div class="logo-container">
                <img src="../assets/img/dc-logo-bg.png" alt="">
            </div>

        </div>
    </footer>
</template>

<style lang="scss" scoped>
@use '../scss/main.scss' as *;

footer {
    display: flex;
    justify-content: center;
    height: 360px;
    width: 100%;
    background-image: url(../assets/img/footer-bg.jpg);
    background-repeat: no-repeat;
    background-size: cover;
    overflow-y: hidden;

    .container {
        display: flex;
        width: 80%;
        height: 100%;
        .footer-nav {
            display: flex;
            width: 50%;
            padding-top: 40px;
            //debug
            // border: 5px solid gold;
            .col{                
                width: 22%;
                ul{
                    margin-bottom: 15px;
                    h4{
                        text-transform: uppercase;
                        color: $light;
                    }
                    li{
                        display: flex;
                        flex-direction: column;
                        margin: 10px 0;
                        a {
                            color: $light-gray;
                            text-transform: capitalize;
                            font-size: $s-txt;
                            transition: all .3s;
                            &:hover {
                                color: $primary;
                            }
                        }
                    }
                }
            }
        }

        .logo-container {
            width: 50%;
            position: relative;
            
            //debug
            // border: 5px solid crimson;

            img {
                position: absolute;
                right: 80px;
                transform: scale(1.2);
            }
        }
    }
}

</style>