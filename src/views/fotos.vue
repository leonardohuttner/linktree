<template>
    <div class="fotos q-pa-md">
        <h6 style="font-size:1.2rem;">Alguns dos nossos Produtos:</h6>
    <q-responsive :ratio="1" style="width: 100%; max-width: 100%;">
        <q-carousel
            animated
            swipeable
            thumbnails
            infinite
            height="100vh"
            autoplay
            v-model="slide"
        >
            <q-carousel-slide :name="1" img-src="/fotos/1.jpg"/>
            <q-carousel-slide :name="2" img-src="/fotos/2.jpg"/>
            <q-carousel-slide :name="3" img-src="/fotos/3.jpg"/>
            <q-carousel-slide :name="4" img-src="/fotos/4.jpg"/>
            <q-carousel-slide :name="5" img-src="/fotos/5.jpg"/>
            <q-carousel-slide :name="6" img-src="/fotos/6.jpg"/>
            <q-carousel-slide :name="7" img-src="/fotos/7.jpg"/>
            <q-carousel-slide :name="8" img-src="/fotos/8.jpg"/>
            <q-carousel-slide :name="9" img-src="/fotos/9.jpg"/>
            <q-carousel-slide :name="10" img-src="/fotos/10.jpg"/>
            <q-carousel-slide :name="11" img-src="/fotos/11.jpg"/>
            <q-carousel-slide :name="12" img-src="/fotos/12.jpg"/>
            <q-carousel-slide :name="13" img-src="/fotos/13.jpg"/>
            <q-carousel-slide :name="14" img-src="/fotos/14.jpg"/>
            <q-carousel-slide :name="15" img-src="/fotos/15.jpg"/>
            <q-carousel-slide :name="16" img-src="/fotos/16.jpg"/>
        </q-carousel>
    </q-responsive>
  </div>
</template>

<script>
export default {
    data(){
        return {
            slide:1
        }
    },
    methods:{
        automatizaSlide(){

        }
    }
}
</script>

<style>
    .fotos{
        height: 100%;
        margin-bottom: 10px;
        padding-bottom: 10px;
    }
</style>