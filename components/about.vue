<template>
  <div class="about-container">
    <div class="wrapper">
      <section>
        <h1 class="text-left uppercase font-bold p-4 px-0 text-3xl">
          Why trust us?
        </h1>
        <p class="text-left">
          Lorem ipsum dolor sit, amet consectetur adipisicing elit. Voluptate
          accusantium sint esse minima quibusdam. Nemo illo doloremque fugit
          error id!
        </p>
        <nuxt-link
          to="/track"
          class="block w-fit bg-gray-300 py-2 px-5 ml-0 mt-3 rounded capitalize"
          >track product</nuxt-link
        >
      </section>
      <div class="absolute-div show-lg">
        <div class="item">
          <div class="content">
            <h2 class="text-left">lorem ipsum</h2>
            <p class="text-left">
              Lorem ipsum dolor sit, amet consectetur adipisicing.
            </p>
          </div>
        </div>
        <div class="item">
          <div class="content">
            <h2>lorem ipsum</h2>
            <p>Lorem ipsum dolor sit, amet consectetur adipisicing.</p>
          </div>
          <div class="content">
            <h2>lorem ipsum</h2>
            <p>Lorem ipsum dolor sit, amet consectetur adipisicing.</p>
          </div>
        </div>
        <div class="item">
          <div class="content">
            <h2>lorem ipsum</h2>
            <p>Lorem ipsum dolor sit, amet consectetur adipisicing.</p>
          </div>
          <div class="content">
            <h2>lorem ipsum</h2>
            <p>Lorem ipsum dolor sit, amet consectetur adipisicing.</p>
          </div>
          <div class="content">
            <h2>lorem ipsum</h2>
            <p>Lorem ipsum dolor sit, amet consectetur adipisicing.</p>
          </div>
        </div>
      </div>
      <div class="absolute-div show-sm">
        <div class="item">
          <div class="content">
            <h2>lorem ipsum</h2>
            <p>Lorem ipsum dolor sit, amet consectetur adipisicing.</p>
          </div>
          <div class="content">
            <h2>lorem ipsum</h2>
            <p>Lorem ipsum dolor sit, amet consectetur adipisicing.</p>
          </div>
          <div class="content">
            <h2>lorem ipsum</h2>
            <p>Lorem ipsum dolor sit, amet consectetur adipisicing.</p>
          </div>
        </div>
        <div class="item">
          <nuxt-link
            to="/track"
            class="block w-fit bg-gray-300 py-2 px-5 ml-0 mt-3 rounded capitalize"
            >track product</nuxt-link
          >
        </div>
        <div class="item">
          <div class="content">
            <h2>lorem ipsum</h2>
            <p>Lorem ipsum dolor sit, amet consectetur adipisicing.</p>
          </div>
          <div class="content">
            <h2>lorem ipsum</h2>
            <p>Lorem ipsum dolor sit, amet consectetur adipisicing.</p>
          </div>
          <div class="content">
            <h2>lorem ipsum</h2>
            <p>Lorem ipsum dolor sit, amet consectetur adipisicing.</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.about-container {
  width: 100%;
  height: fit-content;

  .wrapper {
    width: 90%;
    height: fit-content;
    display: flex;
    justify-content: space-evenly;
    align-items: center;
    position: relative;
    margin: auto;

    section {
      position: relative;
      width: 37%;
      height: fit-content;

      h1 {
        color: rgb(2, 117, 137);
      }
      a {
        background: rgb(2, 117, 137);
        color: white;
      }
    }

    .absolute-div {
      width: 60%;
      min-height: 70vh;
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
        a {
          background: rgb(2, 117, 137);
          color: white;
        }
      }
    }
    .show-sm {
      display: none;
    }

    @media screen and (max-width: 768px) {
      flex-direction: column;

      section {
        width: 100%;

        h1,
        p {
          text-align: center;
        }
        a {
          margin: 20px auto;
        }
      }
      .show-lg {
        display: none;
      }
      .show-sm {
        display: flex;
        width: 100%;
      }
      @media screen and (max-width: 500px) {
        .show-sm {
          flex-direction: column;
          .item {
            flex-direction: row;
            flex-wrap: wrap;

            .content {
              width: 150px;
              flex-grow: 1;
            }
          }
        }
      }
    }
  }
}
</style>
