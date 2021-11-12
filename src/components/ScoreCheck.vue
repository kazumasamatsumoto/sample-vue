<template>
  <div>
    <ion-item>
      <ion-label position="floating">ウォレットアドレス</ion-label>
      <ion-input v-model="address"></ion-input>
    </ion-item>
    <ion-button @click="addressInfo">作成</ion-button>
  </div>
</template>

<script>
  import {
    IonItem,
    IonLabel,
    IonButton,
    IonInput,
  } from "@ionic/vue";
  import { defineComponent, ref } from "vue";

  export default defineComponent({
    components: { IonItem, IonLabel, IonButton, IonInput },
    setup() {
      const address = ref();
      function addressInfo() {
        console.log(address.value, "address");
      }
      return {
        address,
        addressInfo,
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
