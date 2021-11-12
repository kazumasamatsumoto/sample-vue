<template>
  <div>
    <ion-list>
      <ion-item href="/tabs/tab4">
        <ion-label>ブロックチェーンプロジェクト</ion-label>
      </ion-item>
      <ion-item href="/tabs/tab4">
        <ion-label>ビジネスマナー講座</ion-label>
      </ion-item>
    </ion-list>
  </div>
</template>

<script>
  import { IonList, IonItem, IonLabel } from "@ionic/vue";
  import { defineComponent } from "vue";
  export default defineComponent({
    components: { IonList, IonItem, IonLabel },
  });
</script>
