<template>
  <div>
    <Navbar />
    <section class="bg-gray-900">
      <div
        class="max-w-screen-xl px-4 py-32 mx-auto lg:h-screen lg:items-center lg:flex"
      >
        <div class="max-w-xl mx-auto text-center">
          <h1 class="text-3xl text-white font-extrabold sm:text-5xl">
            <!-- Understand User Flow. -->
            <strong class="font-extrabold text-red-400 sm:block">
              An error occurred
            </strong>
          </h1>
          <br />

          <p class="mt-4 sm:leading-relaxed sm:text-xl text-white">
            개발자가 페이지를 만들다 졸았나봐요.. :(
            <br />문제 해결을 위해 저희 개발자에게 이 오류를 알려주세요!
          </p>

          <div class="flex flex-wrap justify-center gap-4 mt-8">
            <NuxtLink
              class="inline-flex w-full px-12 py-3 text-sm font-medium text-white bg-red-600 rounded shadow sm:w-auto active:bg-red-500 hover:bg-red-700 focus:outline-none focus:ring"
              to="/"
            >
              메인 페이지로
              <svg
                class="w-5 h-5 ml-3"
                xmlns="http://www.w3.org/2000/svg"
                fill="none"
                viewBox="0 0 24 24"
                stroke="currentColor"
              >
                <path
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  stroke-width="2"
                  d="M17 8l4 4m0 0l-4 4m4-4H3"
                ></path>
              </svg>
            </NuxtLink>
          </div>
        </div>
      </div>
    </section>
    <Footer />
  </div>
</template>

<script>
export default {
  props: ['error'],
  layout: 'error',
}
</script>
