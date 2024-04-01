<template>
  <main v-if="!loading" class="page">
    <!-- content -->
    <div id="section">
      <div class="services-content services-carousel">
          <div class="item">
            <div class="service-box">
              <div class="img-thumb">
                <img src="/images/projects/ai-resources.png" alt="" class="mb-1">
              </div>
              
              <div class="content">
                  <svg viewBox="0 -20 700 110" width="100%" height="110" preserveAspectRatio="none">
                  <path transform="translate(0, -20)" d="M0,10 c80,-22 240,0 350,18 c90,17 260,7.5 350,-20 v50 h-700" fill="#cac8c9" />
                  <path d="M0,10 c80,-18 230,-12 350,7 c80,13 260,17 350,-5 v100 h-700z" fill="#f0f9fe" />
                </svg>
                <div class="title">
                  <article class="text-wrap">
                    <h1 class="text-sm">THE ORIENTAL BEACH CONDOMINIUM’S GALLERY</h1>
                    <span class="px-1"></span>
                    <p class="text-sm text-wrap">
                      Enjoy a private world carefully crafted for your total relaxation, comfort and enjoyment <br>
                  </p>
                  </article>
                </div>
              </div>
              
            </div>
          </div>

        </div>

      <!-- Image Section1 -->
      <div class="container   mt-8">
        <div class="flex flex-wrap justify-center -mx-5">
          <div id="image-container" class="flex mb-10">
            <img src="/images/projects/ai-resources.png" alt="Image 1" class="w-full max-w-4xl pr-3" />
            <img src="/images/projects/ai-resources.png" alt="Image 2" class="w-full max-w-6xl " />
          </div>
          <div id="image-container" class="flex px-5 mb-10 ">
            <img src="/images/projects/ai-resources.png" alt="Image 3" class="w-full max-w-2xl pr-3" />
            <img src="/images/projects/ai-resources.png" alt="Image 4" class="w-full max-w-8xl pr-96" />
          </div>
          <div id="image-container" class="flex px-5 mb-10 ">
            <img src="/images/projects/ai-resources.png" alt="Image 5" class="w-full max-w-5xl pr-3 pl-40" />
            <img src="/images/projects/ai-resources.png" alt="Image 6" class="w-full max-w-5xl" />
          </div>
        </div>
      </div>
      
      <!-- Image Section 2 -->
      <div id="img">
              <img src="/images/projects/ai-resources.png" alt="">
        </div>
        <div id="img">
              <img src="/images/projects/ai-resources.png" alt="">
        </div>
        <div id="img">
              <img src="/images/projects/ai-resources.png" alt="">
        </div>
        
     <!-- Image Section 3 -->   
    <div id="section" class="overflow-hidden">
      <div class="parent">
        <div class="child1" style="width: 80%;">
          <img src="/images/projects/ai-resources.png" alt="" style="object-fit: cover;">
        </div>
        <div class="child2" style="width: 1%; background-color: #ffffff;">
        </div>
        <div class="child3" style="width: 19%; background-color: #c9c9ca;">
        </div>
      </div>
    </div>

    <div id="section" class="overflow-hidden">
      <div class="parent">
        <div style="width: 19%; background-color: #a0a09f; text-align: center; display: flex; justify-content: center; align-items: center;">
          <p class="p-6 text-lg" style="color: white; font-weight: 100; letter-spacing: 6px; display: inline-block; line-height: 1.5; text-align: left;">
          </p>
        </div>
        <div style="width: 1%; background-color: #ffffff;">
        </div>
        <div style="width: 80%;">
          <img src="/images/projects/ai-resources.png" alt="" style="object-fit: cover;">
        </div>
      </div>

      <div id="section" class="overflow-hidden">
      <div class="parent">
        <div class="child1" style="width: 80%;">
          <img src="/images/projects/ai-resources.png" alt="" style="object-fit: cover;">
        </div>
        <div class="child2" style="width: 1%; background-color: #ffffff;">
        </div>
        <div class="child3" style="width: 19%; background-color: #c9c9ca;">
        </div>
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

#img {
  height: 560px;
  @apply flex justify-center w-full mt-5 
}

.services-content .service-box {
  overflow: hidden;
  position: relative;
}

.services-content.services-carousel .service-box {
    margin-bottom: 30px;
}

.services-content .service-box .img-thumb img {
  aspect-ratio: 16/9;
  object-fit: none;
  width: 100%;
  max-height: 750px;
}

.services-content .service-box .content {
  bottom: 0;
  display: inline-block;
  position: absolute;
  left: 0;
  right: 0;
  text-align: center;
  min-height: 20vw;
  z-index: 1;
}

.services-content .service-box .content .title {
  padding-top: 4vw;
  background-color: #f0f9fe;
  color: #000000;
  min-height: 20vw;
}

.services-content .service-box .content .title h1 {
  font-weight: 100;
  color: gray;
  letter-spacing: 5px;
  @apply  font-fira_retina ;
}

.services-content .service-box .content .title p {
  font-weight: 100;
  line-height: 35px;
  color: gray;
  @apply  font-fira_retina ;
}


.services-content .service-box .content .title a {
    color: #fff;
    position: relative;
    z-index: 9999;
}
</style>