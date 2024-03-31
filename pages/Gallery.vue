<template>
  <main v-if="!loading" class="flex flex-col flex-auto lg:flex-row ">
    <!-- content -->
    <div class="flex flex-col w-full ">
      <!-- projects -->
      <div id="header">
        <div id="img">
          <img src="/images/projects/ai-resources.png" alt="" />
        </div>
        <div class="text-3xl flex justify-center mt-3">
          THE ORIENTAL BEACH CONDOMINIUM'S GALLERY
        </div>
        <div class="flex justify-center">
          <div class="text-center max-w-6xl">
            Enjoy a private world carefully crafted for your total relaxation, comfort and enjoyment
          </div>
        </div>
      </div>

      <!-- Image Divs -->
      <div class="container max-w-6xl mx-auto mt-8">
        <div class="flex flex-wrap justify-center -mx-5">
          <div id="image-container" class="flex px-5 mb-10">
            <img src="/images/projects/ai-resources.png" alt="Image 1" class="w-full max-w-md pr-3" />
            <img src="/images/projects/ai-resources.png" alt="Image 2" class="w-full max-w-md" />
          </div>
          <div id="image-container" class="flex px-5 mb-10 pr-40">
            <img src="/images/projects/ai-resources.png" alt="Image 3" class="w-full max-w-md pr-3" />
            <img src="/images/projects/ai-resources.png" alt="Image 4" class="w-full max-w-md" />
          </div>
          <div id="image-container" class="flex px-5 mb-10 pl-40">
            <img src="/images/projects/ai-resources.png" alt="Image 5" class="w-full max-w-md pr-3" />
            <img src="/images/projects/ai-resources.png" alt="Image 6" class="w-full max-w-md" />
          </div>
        </div>
      </div>
    </div>
  </main>
</template>

<script>
export default {
  setup() {
    const config = useRuntimeConfig();
    return { config };
  },
  data() {
    return {};
  },
  mounted() {
    this.loading = false;
  },
  methods: {},
};
</script>

<style scoped>
#scrollable-section {
  overflow-y: auto;
}

#header {
  min-width: 500px;
  margin-bottom: 5px;
  color: #746c5c;
  @apply font-fira_retina;
}
#title {
  /*border: 1px solid #1E2D3D;*/
  color: #99abb9;
  background-color: #101920;
  border-radius: 0px;
  /* max-width: 400px; */
  /* max-height: 315px; */
}

#container {
  background-color: #746c5c;
}
#img {
   color: #746c5c;
  @apply flex justify-center w-full mt-5 h-80;
}
#showcase {
  border-top-right-radius: 15px;
  border-top-left-radius: 15px;
}
#view-button {
  background-color: #1c2b3a;
}
#view-button:hover {
  background-color: #263b50;
}
#window {
  max-height: 120px;
  position: relative;
  overflow: hidden;
}
</style>