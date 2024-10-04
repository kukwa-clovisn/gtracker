<template>
  <div class="carriers-container">
    <div class="wrapper">
      <h1>Carriers</h1>
      <p class="p-5">
        We're are backed by hundreds or carriers worlwide. <br />
        Including the top-notch carriers you trust the most. We track your
        products from anywhere till it gets to you with constant updates on the
        delivery status.
      </p>
      <div class="flex wrap justify-center items-center">
        <img src="/favicon.ico" alt="" />
        <img src="/favicon.ico" alt="" />
        <img src="/favicon.ico" alt="" />
        <img src="/favicon.ico" alt="" />
        <img src="/favicon.ico" alt="" />
        <img src="/favicon.ico" alt="" />
        <img src="/favicon.ico" alt="" />
        <img src="/favicon.ico" alt="" />
        <img src="/favicon.ico" alt="" />
        <img src="/favicon.ico" alt="" />
        <img src="/favicon.ico" alt="" />
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.carriers-container {
  width: 100vw;
  height: fit-content;
  padding-bottom: 10vh;

  .wrapper {
    width: 90%;
    height: fit-content;
    margin: auto;

    h1 {
      font-size: 40px;
      color: rgb(3, 118, 139);
      font-weight: 700;
    }

    .flex {
      flex-wrap: wrap;
      gap: 20px;
      img {
        height: 140px;
        width: auto;
        object-fit: contain;
        display: block;
        border-radius: 100%;
        box-shadow: 0 0 17px 2px rgb(211, 211, 211);
      }
    }
  }
}
</style>
