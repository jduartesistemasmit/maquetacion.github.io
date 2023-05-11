<template lang="">
<v-container class="mx-1 border rounded-xl elevation-6">
    <v-layout class="text-center font-weight-black">
        <v-row no-gutters>
            <v-col>
                TITULO
            </v-col>
        </v-row>
    </v-layout>
    <v-divider></v-divider>
    <v-layout class="py-3">
        <v-row no-gutters class="d-flex">
            <v-chip class="bg-indigo-darken-4 mx-1 pl-2 pr-6">
                <v-icon icon="mdi mdi-clock-outline"></v-icon> Hora
            </v-chip>
            <v-chip class="bg-indigo-darken-4 mx-1 pl-2 pr-9">
                <v-icon icon="mdi mdi-alpha-n-circle-outline"></v-icon>Numero
            </v-chip>
            <v-chip class="bg-indigo-darken-4 mx-1">Animal</v-chip>
            <v-chip class="bg-indigo-darken-4 mx-1 pl-2 pr-10">
                <v-icon icon="mdi mdi-image-area"></v-icon> Imagen
            </v-chip>
        </v-row>
    </v-layout>
    <v-layout>
        <v-row no-gutters>
            <v-col>
                <v-layout v-for="(_, n) in numero" :key="n">
                    <div class="border rounded-lg ma-1 elevation-4 text-center" style="width:100%; height:75px; line-height: 75px">
                        <strong> {{ secondsToString(Math.floor(Math.random() * (3600*24))) }} </strong>
                    </div>
                </v-layout>
            </v-col>
            <v-col>
                <v-layout v-for="(_, n) in numero" :key="n">
                    <div class="border rounded-lg ma-1 elevation-4 text-center" style="width:100%; height:75px; line-height: 75px">
                        <h1>{{Math.floor(Math.random() * 99)}}</h1>
                    </div>
                </v-layout>
            </v-col>
            <v-col>
                <v-layout v-for="(_, n) in numero" :key="n">
                    <div class="border rounded-lg ma-1 elevation-4 text-center" style="width:100%; height:75px; line-height: 75px">
                        gallina
                    </div>
                </v-layout>
            </v-col>
            <v-col>
                <v-layout v-for="(_, n) in numero" :key="n">
                    <div class="border rounded-lg ma-1 elevation-4 text-center" style="width:100%; height:75px; line-height: 75px">
                        <img src="@/assets/gallina.png" alt="">
                    </div>
                </v-layout>
            </v-col>

        </v-row>
    </v-layout>

</v-container>
</template>

<script>
export default {
    props:{
      numero: {
        type: Number
      }
    },
    methods: {
        randInt() {
            return Math.floor(Math.random() * 99);
        },
        secondsToString(seconds) {
            var hour = Math.floor(seconds / 3600);
            hour = (hour < 10) ? '0' + hour : hour;
            var minute = Math.floor((seconds / 60) % 60);
            minute = (minute < 10) ? '0' + minute : minute;
            return hour + ':' + minute;
        }
    }
}
</script>

<style scoped lang="">

</style>
