<template>
  <div>
    <ion-list>
      <ion-item
        v-for="event in eventList"
        :key="event.id"
        :router-link="`/Event/${event.id}`"
      >
        <ion-label>
          <h2>{{ event.title }}</h2>
          <p>{{ event.id }}</p>
        </ion-label>
      </ion-item>
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
  import { defineComponent, ref } from "vue";
  export default defineComponent({
    components: { IonList, IonItem, IonLabel },
    setup() {
      const eventList = ref([{ id: "1", title: "test" },{ id: "2", title: "test2" }]);
      return {
        eventList,
      };
    },
  });
</script>
