<script setup>
const { query } = useRoute();
console.log(query);
</script>
<template>
  <div class="py-20">
    <h1 class="p-5 text-3xl font-extrabold">Goods Id: {{ query.id }}</h1>
    <div>
      <div class="absolute-div show-sm">
        <div class="item">
          <div class="content">
            <h2>tracking number</h2>
            <p>ABC XXXXXXXXXX XYZ</p>
          </div>
          <div class="content">
            <h2>carrier</h2>
            <p>DHL</p>
          </div>
          <div class="content">
            <h2>description</h2>
            <p>Lorem ipsum dolor sit, amet consectetur adipisicing.</p>
          </div>
        </div>
        <div class="item">
          <div class="content">
            <h2>Purchase Date:</h2>
            <p>Wed. 12 oct 2024</p>
          </div>
          <div class="content">
            <h2>status</h2>
            <p>pending</p>
          </div>
          <div class="content">
            <h2>Days left</h2>
            <p>21</p>
          </div>
        </div>
        <div class="item">
          <div class="content">
            <h2>tracking number</h2>
            <p>ABC XXXXXXXXXX XYZ</p>
          </div>
          <div class="content">
            <h2>carrier</h2>
            <p>DHL</p>
          </div>
          <div class="content">
            <h2>description</h2>
            <p>Lorem ipsum dolor sit, amet consectetur adipisicing.</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.absolute-div {
  width: 100%;
  height: fit-content;
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 10px;

  .item {
    display: flex;
    justify-content: space-between;
    align-items: center;
    flex-direction: column;
    gap: 10px;

    .content {
      width: 100%;
      height: fit-content;
      background: rgb(255, 255, 255);
      box-shadow: 0 0 40px 1px rgb(203, 203, 203);
      border-radius: 4px;
      padding: 20px;

      h2 {
        text-transform: capitalize;
        text-align: left;
        padding-bottom: 5px;
      }

      p {
        text-align: left;

        font-size: 12px;
      }
    }
    span {
      background: rgb(2, 117, 137);
      color: white;
    }
  }
}
</style>
