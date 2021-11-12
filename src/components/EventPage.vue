<template>
  <div class="center">
    <ion-label>
      <h2>イベントID {{ $route.params.id }}</h2>
    </ion-label>
    <h2>{{ eventTitle }}</h2>
    <div class="left">2021/10/8(木)</div>
    <div>
      <h3>担当講師:⚪⚪︎</h3>
    </div>
    <div>
      <p class="left">活動内容</p>
      <div class="center">
        <div class="card2">内容書く</div>
      </div>
      <form>
        <IonButton @click="onClick">参加する</IonButton>
      </form>
      <IonButton @click="goAssessment">テスト</IonButton>
    </div>
  </div>
</template>

<script>
  import { IonLabel, IonButton } from "@ionic/vue";
  import { defineComponent, ref, onMounted } from "vue";
  import { useRoute } from "vue-router";
  export default defineComponent({
    components: { IonLabel, IonButton },
    setup() {
      const route = useRoute();
      const eventTitle = ref();
      onMounted(() => {
        // eslint-disable-next-line no-undef
        console.log(route.params.id);
        if (route.params.id == 1) {
          eventTitle.value = "test";
        } else if (route.params.id == 2) {
          eventTitle.value = "test2";
        }
      });
      function onClick() {
        console.log("clicked!");
      }
      function goAssessment() {
        window.location.href = `Event/${route.params.id}/Assessment`
      }
      const eventList = ref([
        { id: "1", title: "test" },
        { id: "2", title: "test2" },
      ]);
      return {
        eventList,
        eventTitle,
        onClick,
        goAssessment
      };
    },
  });
</script>
<style>
  .card2 {
    width: 400px;
    height: 400px;
    border-radius: 25px;
    background: #aaaaaa;
  }
  .left {
    display: flex;
    flex-direction: column;
    align-items: left;
  }
  .center {
    display: flex;
    flex-direction: column;
    align-items: center;
  }
</style>
