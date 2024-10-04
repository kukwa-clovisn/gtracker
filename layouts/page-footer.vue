<template>
  <footer>
    <div class="mt-4 xl:mt-32 mx-auto w-full relative text-center text-white">
      <div class="px-2 py-4 md:py-4">
        <h2 class="font-bold text-3xl xl:text-4xl leading-snug text-white">
          Ready to get your productivity back?<br />Start your membeship today.
        </h2>
        <nuxt-link
          to="/"
          class="mt-8 xl:mt-12 px-12 py-5 text-lg font-medium leading-tight inline-block bg-orange-500 rounded-full shadow-xl border border-transparent text-white"
          >Get started</nuxt-link
        >
        <div class="mt-14 xl:mt-20">
          <nav
            class="flex flex-wrap justify-center text-lg font-medium text-white"
          >
            <div class="px-5 py-2 text-white">
              <nuxt-link to="/">Home</nuxt-link>
            </div>
            <div class="px-5 py-2 text-white">
              <nuxt-link to="/#about">about us</nuxt-link>
            </div>
            <div class="px-5 py-2 text-white">
              <nuxt-link to="/#values">values</nuxt-link>
            </div>
            <div class="px-5 py-2 text-white">
              <nuxt-link to="/#contact">Contact</nuxt-link>
            </div>
            <div class="px-5 py-2 text-white">
              <nuxt-link to="/#membership">Track product</nuxt-link>
            </div>
            <div class="px-5 py-2 text-white">
              <nuxt-link to="/#about">Privacy</nuxt-link>
            </div>
            <div class="px-5 py-2 text-white">
              <nuxt-link to="/">media links</nuxt-link>
            </div>
          </nav>
          <p class="mt-7 text-base text-gray-300">&copy;GTracker</p>
        </div>
      </div>
    </div>
  </footer>
</template>

<style lang="scss" scoped>
footer {
  width: 100%;
  height: fit-content;
  padding: 20px;
  background: rgb(1, 94, 111);
  background-repeat: no-repeat;
  background-size: cover;
  background-attachment: fixed;
  position: relative;
  background-position: center center;
}
</style>
