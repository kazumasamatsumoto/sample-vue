<template>
  <ion-page>
    <ion-header>
      <ion-toolbar>
        <ion-title>イベント作成</ion-title>
      </ion-toolbar>
    </ion-header>
    <ion-content :fullscreen="true">
      <ion-header collapse="condense">
        <ion-toolbar>
          <ion-title size="large">イベント作成</ion-title>
        </ion-toolbar>
      </ion-header>
      <EventCreate />
    </ion-content>
  </ion-page>
</template>

<script lang="ts">
  import {
    IonPage,
    IonHeader,
    IonToolbar,
    IonTitle,
    IonContent,
  } from "@ionic/vue";
  import EventCreate from "@/components/EventCreate.vue";

  export default {
    name: "Tab3",
    components: {
      EventCreate,
      IonHeader,
      IonToolbar,
      IonTitle,
      IonContent,
      IonPage,
    },
  };
</script>
