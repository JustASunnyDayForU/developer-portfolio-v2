<template>
  <main v-if="!loading" class="page">

    <!-- content -->

    <div id="section">
      <div class="services-content services-carousel">
          <div class="item">
            <div class="service-box">
              <div class="img-thumb">
                <img src="/images/projects/ai-resources.png" alt="">
              </div>
              
              <div class="content">
                  <svg viewBox="0 -20 700 110" width="100%" height="110" preserveAspectRatio="none">
                  <path transform="translate(0, -20)" d="M0,10 c80,-22 240,0 350,18 c90,17 260,7.5 350,-20 v50 h-700" fill="#cac8c9" />
                  <path d="M0,10 c80,-18 230,-12 350,7 c80,13 260,17 350,-5 v100 h-700z" fill="#f0f9fe" />
                </svg>
                <div class="title">
                  <article class="text-wrap">
                    <h1 class="text-sm">THE ORIENTALBEACH CONDOMINIUM</h1>
                    <span class="px-1"></span>
                    <p class="text-sm text-wrap">
                      The Oriental beach condominium is an exclusive development of 50 comdominiums <br>that facilitate the luxury living of your dreams. 
                      The development located between Baan Pae and Laem Mae Pim on the beachside,<br> which means no road or traffic concern, 
                      witha very nice view of Koh Samet.<br>You will have private access to the best beach of Thailand's East Coast 
                      where you<br>can enjoy with very beautiful view of sunrise and sunset
                  </p>
                  </article>
                </div>
              </div>
              
            </div>
          </div>

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

    <div id="section" class="overflow-hidden">
      <div class="parent">
        <div style="width: 70%; background-color: #a0a09f; text-align: center; display: flex; justify-content: center; align-items: center;">
          <p class="p-6 text-lg" style="color: white; font-weight: 100; letter-spacing: 6px; display: inline-block; line-height: 1.5; text-align: left;">
            The special condominium design with the new 
            <br>concept of "zig zag terrace ", which the priva- 
            <br>teterrace of all unitshave nothing above then 
            <br>every units will get the best scenery and the 
            <br>fresh breeze together
          </p>
        </div>
        <div style="width: 1%; background-color: #ffffff;">
        </div>
        <div style="width: 29%;">
          <img src="/images/projects/ai-resources.png" alt="" style="object-fit: cover;">
        </div>
      </div>
    </div>
       
  </main>
</template>

<style scoped>
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

<script>
export default {
  setup() {
    const config = useRuntimeConfig()
    return {
      config
    }
  },
  data() {
    return {
    };
  },
  mounted() {
    this.loading = false;
  },
  methods: {
  },
};

</script>
