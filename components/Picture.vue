<template>
    <v-carousel height="400" show-arrows="hover" cycle hide-delimiter-background>
        <v-carousel-item v-for="(slide, i) in slides" :key="i">
            <v-img :src="slide.image" height="100%" contain>
                <v-container fill-height>
                </v-container>
            </v-img>
        </v-carousel-item>
    </v-carousel>
</template>

<script>
export default {
    data() {
        return {
            slides: [
                { image: 'https://fastly.picsum.photos/id/237/200/300.jpg?hmac=TmmQSbShHz9CdQm0NkEjx1Dyh_Y984R9LpNrpvH2D_U' },
                { image: 'https://fastly.picsum.photos/id/866/200/300.jpg?hmac=rcadCENKh4rD6MAp6V_ma-AyWv641M4iiOpe1RyFHeI' },
                { image: 'https://fastly.picsum.photos/id/894/200/300.jpg?grayscale&hmac=2x_FbywH9y03BbYgR-ngCqp1Jb4OFwWkLT20aCZJlvo' },
                { image: 'https://fastly.picsum.photos/id/870/200/300.jpg?blur=2&grayscale&hmac=ujRymp644uYVjdKJM7kyLDSsrqNSMVRPnGU99cKl6Vs' },
                { image: 'https://fastly.picsum.photos/id/966/200/300.jpg?blur=2&hmac=zxHkH6p_SznoNdebmDuTlIrNyfchhrreyhKrNzxRtkI' },
            ],
        }
    },
}
</script>

<style scoped></style>