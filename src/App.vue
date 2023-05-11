<template>
    <v-alert height="10px">
        <RelojDigital />
    </v-alert>
    <swiper :slidesPerView="5" :spaceBetween="0" :autoplay="{
        delay: 2500,
        disableOnInteraction: true,
    }" :pagination="{
    clickable: true,
}" :breakpoints="{
    '100': { slidesPerView: 1, spaceBetween: 0, },
    '640': { slidesPerView: 2, spaceBetween: 0, },
    '1024': { slidesPerView: 3, spaceBetween: 0, },
    '1400': { slidesPerView: 5, spaceBetween: 0, },
    '2500': { slidesPerView: 6, spaceBetween: 0, },
}" :navigation="true" :modules="modules" :rewind="true" class="mySwiper">
        <swiper-slide>
            <v-container>
                <v-row class="my-4">
                    <CardLotery :numero=3 />
                </v-row>
                <v-row>
                    <CardLotery :numero=3 />
                </v-row>
            </v-container>
        </swiper-slide>
        <swiper-slide>
            <CardLotery :numero=7 />
        </swiper-slide>
        <swiper-slide>
            <v-container>
                <v-row class="my-2">
                    <CardLotery :numero=2 />
                </v-row>
                <v-row  class="my-2">
                    <CardLotery :numero=2 />
                </v-row >
                <v-row  class="my-2">
                    <CardLotery :numero=2 />
                </v-row>
            </v-container>
        </swiper-slide>
        <swiper-slide>
            <CardLotery :numero=8 />
        </swiper-slide>
        <swiper-slide>
            <CardLotery :numero=9 />
        </swiper-slide>
        <swiper-slide>
            <CardLotery :numero=3 />
        </swiper-slide>
        <swiper-slide>
            <CardLotery :numero=1 />
        </swiper-slide>
    </swiper>

    <v-alert height="10px">Incididunt exercitation veniam enim tempor sunt magna ad ex mollit labore exercitation qui eu
        exercitation qui. Cupidatat aliqua cupidatat sint nostrud commodo adipisicing. Commodo et consectetur et consectetur
        minim duis esse ipsum ea ad. Amet esse incididunt adipisicing consequat.</v-alert>
</template>

<script>
// Import Swiper Vue.js components
import { Swiper, SwiperSlide } from 'swiper/vue';
import { Autoplay, Navigation } from 'swiper';
import CardLotery from './components/CardLotery.vue';
import RelojDigital from './components/RelojDigital.vue';
// Import Swiper styles

import 'swiper/css';
import 'swiper/css/pagination';
import 'swiper/css/effect-cards';
// import required modules
import {
    Pagination
} from 'swiper';

export default {
    components: {
        Swiper,
        SwiperSlide,
        CardLotery,
        RelojDigital
    },
    setup() {
        return {
            modules: [Autoplay, Pagination, Navigation],
        };
    },
};
</script>

<style>
#app {
    height: 100%;
}

html,
body {
    position: relative;
    height: 100%;
}

body {
    background: #eee;
    font-family: Helvetica Neue, Helvetica, Arial, sans-serif;
    font-size: 14px;
    color: #000;
    margin: 0;
    padding: 0;
}

.swiper {
    width: 100%;
    height: 100%;
}

.swiper-slide {

    font-size: 18px;
    background: #fff;

    /* Center slide text vertically */
    display: flex;

}

.swiper-slide img {
    display: block;
    width: 100%;
    height: 100%;
    object-fit: cover;
}
</style>
