<script setup>
const trackingNumber = ref("");
const goods = ref(null);

const trackGoods = async () => {
  const response = await fetch(`/api/goods/${trackingNumber.value}`);
  if (response.ok) {
    goods.value = await response.json();
  } else {
    alert("Goods not found");
  }
};
</script>

<template>
  <main>
    <About />
    <Carriers />
  </main>
</template>

<style lang="scss" scoped>
main {
  background: white;
}
</style>
