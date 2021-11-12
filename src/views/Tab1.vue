<template>
  <ion-page>
    <ion-header>
      <ion-toolbar>
        <ion-item href="/tabs/tab1">
          <ion-title>イベント一覧</ion-title>
        </ion-item>
      </ion-toolbar>
    </ion-header>
    <ion-content :fullscreen="true">
      <ion-header collapse="condense">
        <ion-toolbar>
          <ion-title size="large">イベント一覧</ion-title>
        </ion-toolbar>
      </ion-header>
      <EventList />
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
    IonItem,
  } from "@ionic/vue";
  import EventList from "@/components/EventList/index.vue";

  export default {
    name: "Tab1",
    components: {
      EventList,
      IonHeader,
      IonToolbar,
      IonTitle,
      IonContent,
      IonPage,
      IonItem,
    },
  };
</script>
