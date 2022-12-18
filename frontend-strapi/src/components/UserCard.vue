<template>
    <ion-item v-for="cards in card" :key="cards.id">
        <ion-card>
            <img :src="cards.cardImg" />
            <ion-card-header>
                <ion-card-title>{{cards.cardTitle}}</ion-card-title>
                <ion-card-subtitle>{{cards.cardSubtitle}}</ion-card-subtitle>
            </ion-card-header>
    
            <ion-card-content>
                {{cards.cardDsc}}
            </ion-card-content>
        </ion-card>
    </ion-item>
</template>
<script lang="ts">
import {IonCard, IonCardHeader, IonCardTitle, IonCardSubtitle } from '@ionic/vue';
import { defineComponent} from 'vue';
import axios from 'axios';

export default defineComponent({
    components: {
        IonCard, 
        IonCardHeader, 
        IonCardTitle, 
        IonCardSubtitle,
    },
    data(){
        return{
            card: '',
        }
    },
    methods:{
        getPost(){
            axios.get('http://localhost:1337/api/user-cards').then((response) =>{
                this.card = response.data
                console.log('test')
            }).catch((error)=>{
                console.log(error);
            })
        }
    },
    mounted(){
        this.getPost();
    }

});



</script>
<style>
ion-card-header.ios {
    display: flex;
    flex-flow: column-reverse;
}
</style>