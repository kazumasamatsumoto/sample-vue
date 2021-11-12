<template>
  <ion-page>
    <ion-header>
      <ion-toolbar>
        <ion-item href="/tabs/tab1">
          <ion-title>イベント一覧へ戻る</ion-title>
        </ion-item>
      </ion-toolbar>
    </ion-header>
    <ion-content :fullscreen="true">
      <ion-header collapse="condense">
        <ion-toolbar>
          <ion-title size="large">イベント一覧</ion-title>
        </ion-toolbar>
      </ion-header>

      <Event />
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
  import Event from "@/components/EventPage/index.vue";

  export default {
    name: "Tab4",
    components: { Event, IonHeader, IonToolbar, IonTitle, IonContent, IonPage, IonItem },
  };
</script>
