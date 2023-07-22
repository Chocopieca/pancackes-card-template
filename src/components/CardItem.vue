<template>
  <div class="wrapper-block main-dark-purple border main-green-border overflow-hidden">
    <div class="main-light-purple d-flex justify-space-between pa-2">
      <div class="d-flex">
        <img src="/src/assets/img/play-circle-outline.png" alt="hui" class="mr-1">
        <div class="size16-weight700">LIVE</div>
      </div>
      <div class="flex-center">#190936</div>
    </div>
    <div class="card pa-5">
      <div class="card-top text-align-center" @click="isUp = true">
        <div>UP</div>
        <div>1.73x Payout</div>
      </div>
      <div
          class="card-content border"
          :class="getBorderColor"
      >
        <div class="size12-weight700 mb-2">Last Price</div>
        <div class="d-flex justify-space-between mb-4">
          <div class="size24-weight700">$242.7848</div>
          <div class="d-flex">
            <img src="/src/assets/img/play-circle-outline.png" alt="hui" class="mr-1">
            <div>$-0.0436</div>
          </div>
        </div>
        <div class="d-flex justify-space-between size14-weight400">
          <div>Locked Price:</div>
          <div>$242.7934</div>
        </div>
        <div class="d-flex justify-space-between size16-weight700">
          <div>Prize Pool:</div>
          <div>9.4917 BNB</div>
        </div>
      </div>
      <div class="card-bottom text-align-center" @click="isUp = false">
        <div>1.73x Payout</div>
        <div>DOWN</div>
        <!--          <img src="/src/assets/img/figure-2.svg" alt="">-->
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "CardItem",
  data() {
    return {
      isLoading: true,
      isUp: true
    };
  },
  computed: {
    getBorderColor() {
      return this.isUp ? "main-green-border" : "main-pink-border";
    }
  }
}
</script>

<style scoped lang="scss">
.wrapper-block {
  max-width: 320px;
  width: 100%;
  border-radius: 20px;

  img {
    width: 24px;
  }
}
.card {
  &-top {
    background-image: url("/src/assets/img/figure-1.svg");
    background-size: contain;
    background-repeat: no-repeat;
    background-position: center;
    min-height: 65px;
  }
  &-content {
    border-radius: 20px;
    padding: 20px;
    border-width: 3px;
  }
  &-bottom {
    background-image: url("/src/assets/img/figure-2.svg");
    background-size: contain;
    background-repeat: no-repeat;
    background-position: center;
    min-height: 65px;
  }
}
</style>
