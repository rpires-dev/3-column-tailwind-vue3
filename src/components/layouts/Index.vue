<template>
  <!-- Background color split screen for large screens -->
  <div class="fixed top-0 left-0 w-1/2 h-full bg-white" aria-hidden="true" />
  <div class="fixed top-0 right-0 w-1/2 h-full bg-gray-50" aria-hidden="true" />
  <div class="relative min-h-screen flex flex-col">
    <!-- Navbar -->
    <Navbar />
    <!-- 3 column wrapper -->
    <div class="flex-grow w-full max-w-8xl mx-auto xl:px-8 lg:flex">
      <div class="flex-1 min-w-0 bg-white xl:flex">
        <div
          class="border-b border-gray-200 xl:border-b-0 xl:flex-shrink-0 xl:w-64 xl:border-r xl:border-gray-200 bg-white"
        >
          <div class="h-full pl-4 pr-6 py-6 sm:pl-6 lg:pl-8 xl:pl-0">
            <!-- LEFT SIDEBAR -->
            <LeftSidebar />
          </div>
        </div>
        <div class="bg-white lg:min-w-0 lg:flex-1">
          <div class="h-full py-6 px-4 sm:px-6 lg:px-8">
            <!-- MAIN AREA -->
            <Main />
          </div>
        </div>
      </div>
      <div
        class="bg-gray-50 pr-4 sm:pr-6 lg:pr-8 lg:flex-shrink-0 lg:border-l lg:border-gray-200 xl:pr-0"
      >
        <div class="h-full pl-6 py-6 lg:w-80">
          <!-- RIGHT SIDEBAR -->
          <RightSidebar />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Navbar from "../includes/Navbar.vue";
import LeftSidebar from "../includes/LeftSidebar.vue";
import RightSidebar from "../includes/RightSidebar.vue";
import Main from "../layouts/Main.vue";

export default {
  components: {
    Navbar,
    LeftSidebar,
    RightSidebar,
    Main,
  },
};
</script>
