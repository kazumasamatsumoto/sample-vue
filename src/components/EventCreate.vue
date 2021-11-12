<template>
  <div>
    <ion-item>
      <ion-label position="floating">イベント名</ion-label>
      <ion-input></ion-input>
    </ion-item>
    <ion-item>
      <ion-label position="floating">開催日</ion-label>
      <ion-datetime display-format="YYYY/MM/D H:mm" min="1997" max="2010" value="2021-11-10T12:00Z"></ion-datetime>
    </ion-item>
    <ion-item>
      <ion-label position="floating">終了日</ion-label>
      <ion-datetime display-format="YYYY/MM/D H:mm" min="1997" max="2010" value="2021-11-10T12:00Z"></ion-datetime>
    </ion-item>
    <ion-item>
      <ion-label position="floating">申し込み締切日</ion-label>
      <ion-datetime display-format="YYYY/MM/D H:mm" min="1997" max="2010" value="2021-11-10T12:00Z"></ion-datetime>
    </ion-item>
    <ion-item>
      <ion-label position="floating">講師氏名</ion-label>
      <ion-input></ion-input>
    </ion-item>
    <ion-item>
      <ion-label position="floating">イベント詳細</ion-label>
      <ion-textarea
        rows="6"
        cols="20"
        placeholder="Enter any notes here..."
      ></ion-textarea>
    </ion-item>
    <ion-button>作成</ion-button>
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
  import { defineComponent } from "vue";
  import { Calendar } from "@ionic-native/calendar";

  export default defineComponent({
    components: { IonItem, IonLabel, IonTextarea, IonButton, IonInput, IonDatetime },
    setup() {
      const create = () => {
        Calendar.createCalender("MyCalender").then(
          (msg) => {
            console.log(msg);
          },
          (err) => {
            console.log(err);
          }
        );
      };
      return {
        create
      }
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
