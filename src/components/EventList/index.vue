<template>
  <div>
    <div class="center">
      <u>
        <h1>イベント一覧</h1>
      </u>
    </div>
    <div class="center">
      <div class="card2">
        <div class="center">
          <ion-button href="/tabs/tab4">ブロックチェーンプロジェクト</ion-button>
          <ion-button href="/tabs/tab4">ビジネスマナー講座</ion-button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
  import {
    IonButton,
  } from "@ionic/vue";
  import { defineComponent } from "vue";
  export default defineComponent({
    components: { IonButton },
  });
</script>

<style>
  .container {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
  }

  .card2 {
    width: 400px;
    height: 400px;
    border-radius: 25px;
    background: #aaaaaa;
  }
  .center {
    display: flex;
    flex-direction: column;
    align-items: center;
  }
</style>
