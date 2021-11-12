<template>
  <ion-page>
    <ion-header>
      <ion-toolbar>
        <ion-title>スコア確認</ion-title>
      </ion-toolbar>
    </ion-header>
    <ion-content :fullscreen="true">
      <ion-header collapse="condense">
        <ion-toolbar>
          <ion-title size="large">スコア確認</ion-title>
        </ion-toolbar>
      </ion-header>
      <ScoreCheck />
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
  import ScoreCheck from "@/components/ScoreCheck.vue"

  export default {
    name: "Tab2",
    components: {
      ScoreCheck,
      IonHeader,
      IonToolbar,
      IonTitle,
      IonContent,
      IonPage,
    },
  };
</script>
