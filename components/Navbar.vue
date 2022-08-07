<template>
  <header class="bg-gray-900">
    <div class="max-w-screen-xl px-4 mx-auto sm:px-6 lg:px-8">
      <div class="flex items-center justify-between h-16">
        <div class="flex-1 md:flex md:items-center md:gap-12">
          <a class="flex items-center text-white" href="/"
            ><span class="sr-only">Home</span>
            <!-- <img src="/logo.png" class="h-8 mr-2 rounded-full" loading="lazy" /> -->
            <span>Esoft, korea</span></a
          >
        </div>
        <div class="md:flex md:items-center md:gap-8">
          <nav class="hidden md:block" aria-labelledby="header-navigation">
            <h2 class="sr-only" id="header-navigation">Header navigation</h2>
            <ul class="flex items-center gap-6 text-s">
              <li>
                <a
                  class="text-white transition hover:text-white/75"
                  href="https://api.esoftkorea.co.kr/"
                  >API</a
                >
              </li>
              <li>
                <NuxtLink
                  class="text-white transition hover:text-white/75"
                  to="/recruit"
                  >Recruit</NuxtLink
                >
              </li>
              <li>
                <a
                  class="text-white transition hover:text-white/75"
                  href="https://file.esoftkorea.co.kr"
                  >File Upload</a
                >
              </li>
              <li>
                <a
                  class="text-white transition hover:text-white/75"
                  href="https://dstm.esoftkorea.co.kr"
                  >DSTM</a
                >
              </li>
            </ul>
          </nav>
          <div class="flex items-center gap-4">
            <div class="sm:gap-4 sm:flex">
              <NuxtLink
                class="px-5 py-2.5 text-sm font-medium text-white bg-indigo-500 rounded-md shadow"
                to="/discord"
                >Discord</NuxtLink
              >
            </div>
          </div>
        </div>
      </div>
    </div>
  </header>
</template>
