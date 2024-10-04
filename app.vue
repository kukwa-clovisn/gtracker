<script setup>
useHead({
  title: "Gtracker",
  viewport: "width:device-width, initial-scale=1",
  charset: "utf-8",
  meta: [
    {
      name: "description",
      content:
        "Track your goods online at the comfort of your home with ease and confidence.",
    },
  ],
  link: [
    {
      rel: "icon",
      type: "image/png",
      href: "/favicon.ico",
    },
    {
      href: "https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.1.1/css/all.min.css",
      rel: "stylesheet",
      integrity:
        "sha512-KfkfwYDsLkIlwQp6LFnl8zNdLGxu9YAA1QvwINks4PhcElQSvqcyVLLD9aMhXd13uQjoXtEKNosOWaZqXgel0g==",
      crossorigin: "anonymous",
      referrerpolicy: "no-referrer",
    },
    {
      rel: "preconnect",
      href: "https://fonts.gstatic.com",
      crossorigin: "anonymous",
    },
    {
      href: "https://fonts.googleapis.com/css2?family=Montserrat:wght@100;200;300;400;500;600;700;800;900&family=Nunito+Sans:wght@200;300;400;600;700;800;900&family=Poppins:wght@100;200;300;400;500;600;700;800;900&display=swap",
      rel: "stylesheet",
    },
    {
      href: "https://fonts.googleapis.com/css?family=Material+Icons|Material+Icons+Outlined|Material+Icons+Two+Tone|Material+Icons+Round|Material+Icons+Sharp",
      rel: "stylesheet",
    },
  ],
});
</script>
<template>
  <NuxtLayout>
    <main>
      <h1 class="font-extrabold text-white">
        Flexible and trusted tracking of your products.
      </h1>
      <div class="buttons">
        <nuxt-link to="/track">track product</nuxt-link>
        <nuxt-link to="/track/add">add product</nuxt-link>
      </div>
      <nav>
        <div class="wrapper">
          <nuxt-link to="/goods">goods</nuxt-link>
          <nuxt-link to="/track">tracking</nuxt-link>
          <nuxt-link to="/updates">updates</nuxt-link>
          <nuxt-link to="/shipping">shipping</nuxt-link>
          <nuxt-link to="/status">status</nuxt-link>
          <nuxt-link to="/details">details</nuxt-link>
        </div>
      </nav>
    </main>
    <NuxtPage />
  </NuxtLayout>
</template>

<style lang="scss" scoped>
main {
  width: 100vw;
  height: auto;
  padding-top: 15vh;
  background: rgb(1, 94, 111);
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 30px;
  flex-direction: column;

  h1 {
    font-size: 35px;
    text-align: center;
    text-transform: capitalize;
    padding: 20px;
  }

  .buttons {
    width: fit-content;
    padding: 10px;
    box-shadow: 0 0 1px 1px white;
    background: rgb(2, 117, 137);
    display: flex;
    justify-content: center;
    align-items: center;
    flex-wrap: wrap;
    gap: 10px;
    border-radius: 9px;

    a {
      min-width: 190px;
      height: 40px;
      border-radius: 5px;
      background: inherit;
      color: white;
      display: flex;
      justify-content: center;
      font-weight: 600;
      align-items: center;
      text-transform: capitalize;

      &:first-child {
        background: white;
        color: rgb(0, 12, 18);
      }

      @media screen and (max-width: 460px) {
        min-width: fit-content;
        font-size: 12px;
        padding: 0 20px;

        @media screen and (max-width: 303px) {
          padding: 0 7px;
        }
      }
    }
  }

  nav {
    width: 100%;
    height: 9vh;
    background: rgb(3, 118, 139);

    .wrapper {
      width: 100%;
      height: 100%;
      display: flex;
      justify-content: space-evenly;
      align-items: center;

      a {
        height: 100%;
        width: 100%;
        display: flex;
        justify-content: center;
        align-items: center;
        padding: 0 10px;
        text-transform: capitalize;
        font-weight: 600;
        color: white;
        font-size: 18px;

        @media screen and (max-width: 650px) {
          font-size: 14px;

          @media screen and (max-width: 500px) {
            width: auto;
            height: 8vh;
            flex-grow: 1;
          }
        }
      }
    }
    @media screen and (max-width: 500px) {
      height: fit-content;
      .wrapper {
        flex-wrap: wrap;

        flex-basis: auto;
      }
    }
  }
}

a.router-link-active.router-link-exact-active {
  background: white;
  color: black;

  &:hover {
    transform: scale(1);
  }
}
</style>
