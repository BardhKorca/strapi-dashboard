<template>
  <ion-menu content-id="main-content">
    <ion-header>
      <ion-toolbar>
        <ion-title>Menu Content</ion-title>
      </ion-toolbar>
    </ion-header>
    <ion-content class="ion-padding">
        <a href="#">test</a>
        <br>
        <a href="#">test</a>
        <br>
        <a href="#">test</a>
        <br>
        <a href="#">test</a>
    </ion-content>
  </ion-menu>
</template>
<script lang="ts">
// import Dashboard from '../views/DashboardView.vue';
// import HomePage from '../views/HomePage.vue';
// import SignIn from '../views/SignIn.vue';

import {
    IonContent,
    IonHeader,
    IonMenu,
    IonTitle,
    IonToolbar
  } from '@ionic/vue';  
import { defineComponent } from 'vue';

export default defineComponent({
  components: {
      IonContent,
      IonHeader,
      IonMenu,
      IonTitle,
      IonToolbar
  }
});
</script>