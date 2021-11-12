<template>
  <div>
    <ion-item>
      <ion-label position="floating">ウォレットアドレス</ion-label>
      <ion-input></ion-input>
    </ion-item>
    <ion-button>作成</ion-button>
  </div>
</template>

<script>
  import {
    IonItem,
    IonLabel,
    IonButton,
    IonInput,
  } from "@ionic/vue";
  import { defineComponent } from "vue";
  import { Calendar } from "@ionic-native/calendar";

  export default defineComponent({
    components: { IonItem, IonLabel, IonButton, IonInput },
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
