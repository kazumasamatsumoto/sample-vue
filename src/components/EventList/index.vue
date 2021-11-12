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
          <form v-on:submit="$router.push('/eventpage')">
            <button>ブロックチェーンプロジェクト</button>
          </form>
          <form v-on:submit="$router.push('/eventpage')">
            <button>ビジネスマナー講座</button>
          </form>
        </div>
      </div>
    </div>
  </div>
  
</template>

<script>
export default {
  props: {
    user: Object
  }
};


</script>

<style>

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