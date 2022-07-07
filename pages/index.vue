<template>
  <div>
    <!-- 내비게이션 바 -->
    <Navbar />

    <!-- 메인 헤더 -->
    <section class="text-white bg-gray-900">
      <div
        class="max-w-screen-xl px-4 py-32 mx-auto lg:h-screen lg:items-center lg:flex"
      >
        <div class="max-w-3xl mx-auto text-center">
          <h1
            class="text-3xl font-extrabold text-transparent sm:text-5xl bg-clip-text bg-gradient-to-r from-green-300 via-blue-500 to-purple-600 !leading-tight"
          >
            새로운 미래로 도약하다.<span class="hidden sm:block"
              >Esoft, korea</span
            >
          </h1>
          <p class="max-w-xl mx-auto mt-4 sm:leading-relaxed sm:text-xl">
            작은 영향력을 모아 새로운 미래로 도약하는 Esoft, korea입니다.
          </p>
          <div class="flex flex-wrap justify-center gap-4 mt-8">
            <NuxtLink
              class="block w-full px-12 py-3 text-sm font-medium text-white bg-indigo-500 border border-indigo-500 rounded sm:w-auto active:text-opacity-75 hover:bg-transparent hover:text-white focus:outline-none focus:ring"
              to="/discord"
              >Discord</NuxtLink
            ><NuxtLink
              class="block w-full px-12 py-3 text-sm font-medium text-white border border-indigo-500 rounded sm:w-auto hover:bg-indigo-500 active:bg-indigo-500 focus:outline-none focus:ring"
              to="/recruit"
              >Recruit</NuxtLink
            >
          </div>
        </div>
      </div>
    </section>

    <!-- 팀원 -->
    <section class="text-white bg-gray-900">
      <div class="max-w-screen-xl px-4 py-16 mx-auto sm:px-6 lg:px-8">
        <div class="max-w-lg mx-auto text-center">
          <h2 class="text-3xl font-bold sm:text-4xl">Esoft, Korea 팀원</h2>
          <p class="mt-4 text-gray-300">
            저희 Esoft, Korea에서 일하시는 팀원을 확인하세요.
          </p>
        </div>

        <div class="grid grid-cols-1 gap-8 mt-8 md:grid-cols-2 lg:grid-cols-3">
          <div
            class="block p-8 transition border border-gray-800 shadow-xl rounded-xl hover:shadow-pink-500/10 hover:border-pink-500/10"
            v-for="data in this.crew.json"
            :key="data"
          >
            <img
              class="w-10 h-10 rounded-full"
              :src="
                'https://cdn.discordapp.com/avatars/' +
                data.id +
                '/' +
                data.avatar +
                '.png'
              "
              alt="profile image"
              loading="lazy"
            />
            <h3 class="mt-4 text-xl font-bold text-white">
              {{ data.user_tag }}
            </h3>
            <p class="mt-1 text-sm text-gray-300">
              {{ data.position }}
            </p>
          </div>
        </div>

        <div class="mt-12 text-center">
          <NuxtLink
            class="inline-flex items-center px-8 py-3 mt-8 text-white bg-indigo-500 border border-indigo-500 rounded hover:bg-transparent active:text-indigo-500 focus:outline-none focus:ring"
            to="/recruit"
            ><span class="text-sm font-medium"> Recruit </span
            ><svg
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
    </section>
    <div class="hidden md:flex w-full justify-center bg-gray-900">
      <iframe
        src="https://business.esoftkorea.co.kr/forms/"
        style="border: 0; width: 930px; height: 150px"
        scrolling="no"
      ></iframe>
    </div>

    <!-- 푸터 -->
    <Footer />
  </div>
</template>

<script>
import * as crew from '../static/crew.json'

export default {
  name: 'IndexPage',
  data() {
    return { crew: JSON.parse(JSON.stringify(crew)).default }
  },
}
</script>
