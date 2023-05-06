<script>
export default {
    name: 'Card',
    props: {
        Thumb   : String,
        Series  : String,
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

    </div>

</template>

<style lang="scss" scoped>
@use '../../scss/main.scss' as *;
.card {
    width: calc(100% / 6 - 20px);
    padding: 0 10px;
    margin: 15px 10px;
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
}
</style>