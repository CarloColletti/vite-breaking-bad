<script>
export default {
    props: {
        immagine: String,
        titolo: String,
        archetipo: String,
    },
};
</script>

<template>
    <div class="col d-flex flex-column text-center py-3">
        <div class="carta-back">
            <img :src="immagine" alt="#" />
            <div class="testo-carta py-2">
                <h2 class="my-2 fs-5">{{ titolo }}</h2>
                <span class="my-1">{{ archetipo }}</span>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
.carta-back {
    background-color: #d48f3a;

        .testo-carta{
            height: 100%;
            
            h2 {
                color: white;
            }
        
            span {
                font-weight: bold;
            }
        }

}
</style>
