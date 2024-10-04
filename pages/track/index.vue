<script setup>
const trackingNumber = ref("");
const description = ref("");
const location = ref("");
const status = ref("pending");
const Carrier = ref("");

const addGoods = async () => {
  const response = await fetch("/api/goods", {
    method: "POST",
    headers: {
      "Content-Type": "application/json",
    },
    body: JSON.stringify({
      trackingNumber: trackingNumber.value,
      description: description.value,
      location: location.value,
      status: status.value,
    }),
  });
  if (response.ok) {
    alert("Goods added successfully!");
    trackingNumber.value = "";
    description.value = "";
    location.value = "";
    status.value = "pending";
  } else {
    alert("Failed to add goods");
  }
};
</script>
<template>
  <div class="tracking-container">
    <h1>Fill in your product details below</h1>
    <form
      @submit.prevent="addGoods"
      class="w-fit h-fit p-3 m-auto my-5 flex flex-col justify-center items-start gap-5"
    >
      <input
        v-model="trackingNumber"
        placeholder="Tracking Number - { ABC-12345678-ZX
  }"
        required
      />
      <input v-model="Carrier" placeholder="Carrier" required />
      <input v-model="description" placeholder="Description" required />
      <input v-model="location" placeholder="Location" required />
      <select v-model="carrier">
        <option value="dhl">DHL</option>
        <option value="fedex">FedEx</option>
        <!-- Add more carriers as needed -->
      </select>
      <button type="submit" class="p-2 px-6 bg-gray-300 rounded">Submit</button>
    </form>
  </div>
</template>

<style lang="scss" scoped>
.tracking-container {
  width: 100vw;
  height: fit-content;
  padding-top: 5vh;

  form {
    width: fit-content;
    height: fit-content;
    padding: 20px;
    margin: 20px auto;
    input {
      width: 500px;
      height: 40px;
      outline: none;
      padding: 4px 14px;
      border: 1px solid rgb(151, 151, 151);
      border-radius: 2px;
    }
    @media screen and (max-width: 600px) {
      width: 98%;

      input {
        width: 90%;
      }
    }
  }
}
</style>
