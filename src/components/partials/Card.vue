<script>
export default {
    name: 'Card',
    props: {
        Thumb   : String,
        Series  : String,
        Type    : String,
        Price   : Number
    }
}
</script>

<template>
    
    <div class="card">

        <div class="image-container">
            <img :src="Thumb" alt="comic-thumb">
        </div>
        
        <div class="txt-container">
            <span>{{Series}}</span>
        </div>

        <div class="other-info-container">
            <h5>{{ Type }}</h5>
            <h5>${{ Price }}</h5>
        </div>

    </div>

</template>

<style lang="scss" scoped>
@use '../../scss/main.scss' as *;
.card {
    width: calc(100% / 6 - 20px);
    padding: 0 10px;
    margin: 15px 10px;
    transition: all 0.5s;
    cursor: pointer;
    &:hover {
        transform: scale(1.1);
    }
    .image-container {
        width: 100%;
        aspect-ratio: 2/3;
        margin-bottom: 10px;
        img{
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
    }
    .txt-container {
        display: flex;
        justify-content: center;
        align-items: center;
        span{
            text-transform: uppercase;
            font-weight: $light-bold;
            color: $light;
        }
    }
    
    .other-info-container {
        display: flex;
        flex-direction: column;
        justify-content: center;
        color: $light;
        
        h5{
            &:first-child{
                text-transform: capitalize;
            }
        }
    }
}
</style>