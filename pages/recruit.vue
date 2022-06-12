<template>
  <div>
    <!-- 내비게이션 바 -->
    <Navbar />

    <div
      class="flex flex-col h-screen gap-8 justify-center text-center bg-gray-900"
    >
      <div class="mx-auto">
        <div class="flex justify-center items-center mb-6">
          <div
            class="loader ease-linear rounded-full border-8 border-t-8 border-gray-300 h-28 w-28"
          ></div>
        </div>
      </div>
      <p class="text-gray-100 text-xl">Loading...</p>
    </div>

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

<style scoped>
/* spinner */
.loader {
  border-top-color: #ffdd74;
  -webkit-animation: spinner 1.5s linear infinite;
  animation: spinner 1.5s linear infinite;
}

@-webkit-keyframes spinner {
  0% {
    -webkit-transform: rotate(0deg);
  }

  100% {
    -webkit-transform: rotate(360deg);
  }
}

@keyframes spinner {
  0% {
    transform: rotate(0deg);
  }

  100% {
    transform: rotate(360deg);
  }
}
</style>

<script>
export default {
  name: 'RecruitPage',
  mounted: () => {
    location.replace('https://forms.gle/s555uuasuLuSWydc6')
  },
}
</script>
