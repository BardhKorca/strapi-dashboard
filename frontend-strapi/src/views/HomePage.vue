<template>
  <MenuBox/>
  <ion-page id="main-content">
    <ion-header>
      <ion-toolbar>
        <ion-buttons slot="start">
          <ion-menu-button></ion-menu-button>
        </ion-buttons>
        <ion-title>Menu</ion-title>
      </ion-toolbar>
    </ion-header>
    
    <UserCard/>
  </ion-page>

</template>
<script lang="ts">
// import Dashboard from '../views/DashboardView.vue';
// import HomePage from '../views/HomePage.vue';
// import SignIn from '../views/SignIn.vue';

import {
    IonButtons,
    IonHeader,
    IonMenuButton,
    IonPage,
    IonTitle,
    IonToolbar,
  } from '@ionic/vue';  
import { defineComponent } from 'vue';
import MenuBox from '@/components/MenuBox.vue'
import UserCard from '@/components/UserCard.vue';

export default defineComponent({
  components: {
    IonButtons,
      IonHeader,
      IonMenuButton,
      IonPage,
      IonTitle,
      IonToolbar,
      MenuBox,
      UserCard,
  }
});
</script>