<template>
  <div class="center">
    <div>イベントページ</div>
    <h2>ブロックチェーンプロジェクト</h2>
    <div class="left">2021/10/8(木)</div>
    <div>
      <h3>担当講師:⚪⚪︎</h3>
    </div>
    <div>
      <p class="left">活動内容</p>
      <div class="center">
        <div class="card2">
          内容書く
        </div>
      </div>
      <form>
        <IonButton @click="onClick">参加する</IonButton>
      </form>
    </div>
  </div>
</template>

<script>
import { IonButton } from '@ionic/vue';
export default {
  props: {
    user: Object
  },
  components: { IonButton },
  methods: {
    onClick: () => {
      console.log('click')
    }
  },
};
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