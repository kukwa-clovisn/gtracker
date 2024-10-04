<template>
  <div class="pt-16 pb-20">
    <h1 class="font-bold text-2xl p-5">
      All the goods you are tracking will appear here!
    </h1>

    <div class="container">
      <table class="table w-11/12 m-auto border p-0">
        <thead
          class="p-2 flex justify-between items-center border border-t-0 border-gray-400 py-6 cursor-pointer font-bold bg-gray-800"
        >
          <span class="font-bold text-white">index</span>
          <span class="font-bold text-white">Product Name</span>
          <span class="font-bold text-white">Date</span>
          <span class="font-bold text-white">Status</span>
          <span class="font-bold text-white">Details</span>
        </thead>
        <td
          v-for="i in 10"
          :key="i"
          class="p-2 flex justify-between items-center border border-gray-100 py-6"
        >
          <span>{{ i }}</span> <span>Product Name{{ i }}.</span>
          <span>Tuesday 06 Nov 20024</span>
          <span>pending</span>
          <button @click="navigateTo(`/details?id=${i}`)">Details</button>
        </td>
      </table>
    </div>
  </div>
</template>

<style lang="scss" scoped>
table {
  td {
    text-transform: capitalize;

    button {
      padding: 3px 10px;
      border-radius: 5px;
      background: rgb(20, 20, 20);
      color: white;
    }

    &:nth-child(odd) {
      background: rgb(228, 235, 235);
    }
  }
}
</style>
