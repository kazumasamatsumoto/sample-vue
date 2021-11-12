<template>
  <div>
    <ion-item>
      <ion-label position="floating">イベント名</ion-label>
      <ion-input v-model="eventName"></ion-input>
    </ion-item>
    <ion-item>
      <ion-label position="floating">開催日</ion-label>
      <ion-datetime
        display-format="YYYY/MM/D H:mm"
        min="2021"
        max="2022"
        value="2021-11-10T12:00Z"
        placeholder="2021-11-10T12:00Z"
        v-model="startAt"
      ></ion-datetime>
    </ion-item>
    <ion-item>
      <ion-label position="floating">終了日</ion-label>
      <ion-datetime
        display-format="YYYY/MM/D H:mm"
        min="2021"
        max="2022"
        value="2021-11-10T12:00Z"
        placeholder="2021-11-10T12:00Z"
        v-model="endAt"
      ></ion-datetime>
    </ion-item>
    <ion-item>
      <ion-label position="floating">申し込み締切日</ion-label>
      <ion-datetime
        display-format="YYYY/MM/D H:mm"
        min="2021"
        max="2022"
        value="2021-11-10T12:00Z"
        placeholder="2021-11-10T12:00Z"
        v-model="deadlineAt"
      ></ion-datetime>
    </ion-item>
    <ion-item>
      <ion-label position="floating">講師氏名</ion-label>
      <ion-input v-model="teachersName"></ion-input>
    </ion-item>
    <ion-item>
      <ion-label position="floating">イベント詳細</ion-label>
      <ion-textarea
        rows="6"
        cols="20"
        placeholder="Enter any notes here..."
        v-model="eventDescription"
      ></ion-textarea>
    </ion-item>
    <ion-button @click="createEvent">作成</ion-button>
  </div>
</template>

<script>
  import {
    IonItem,
    IonLabel,
    IonTextarea,
    IonButton,
    IonInput,
    IonDatetime,
  } from "@ionic/vue";
  import { defineComponent, ref } from "vue";

  export default defineComponent({
    components: {
      IonItem,
      IonLabel,
      IonTextarea,
      IonButton,
      IonInput,
      IonDatetime,
    },
    setup() {
      const eventName = ref();
      const startAt = ref();
      const endAt = ref();
      const deadlineAt = ref();
      const teachersName = ref();
      const eventDescription = ref();

      function createEvent() {
        console.log(eventName.value, "eventName");
        console.log(startAt.value, "startAt");
        console.log(endAt.value, "endAt");
        console.log(deadlineAt.value, "deadlineAt");
        console.log(teachersName.value, "teachersName");
        console.log(eventDescription.value, "eventDescription");
      }
      return {
        eventName,
        startAt,
        endAt,
        deadlineAt,
        teachersName,
        eventDescription,
        createEvent,
      };
    },
  });
</script>

<style>
  .card {
    width: 400px;
    height: 100px;
    border-radius: 25px;
    background: #aaaaaa;
  }
  .center {
    display: flex;
    flex-direction: column;
    align-items: center;
  }
</style>
