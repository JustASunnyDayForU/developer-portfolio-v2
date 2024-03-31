<template>
  <main v-if="!loading" class="flex flex-col flex-auto lg:flex-row overflow-hidden">

    <!-- content -->

    <div  class="flex flex-col w-full overflow-hidden">
      <!-- projects -->
  
      <div id="header">
          <div id="img">
              <img src="/images/projects/ai-resources.png" alt="">
          </div>

          <div class="text-3xl flex justify-center mt-3">
              MASTER PLAN
          </div>
        </div>

      <div id="content" class="overflow-hidden">
        <div id="title" class="text-3xl flex">
          PENTHOUSE
        </div>
        <div id="img">
              <img src="/images/projects/ai-resources.png" alt="">
        </div>
        <div id="title" class="text-3xl flex">
          DUPLEX
        </div>
        <div id="title" class="text-3xl flex">
          TYPE A
        </div>
        <div id="title" class="text-3xl flex">
          TYPE B
        </div>
        <div id="title" class="text-3xl flex">
          TYPE C
        </div>
        
      </div>
        
    </div>
       
</main>
</template>

<style scoped>

#projects-case {
  /* padding: 100px; */
}

#header {
  min-width: 500px;
  margin-bottom: 5px;
  color: #746c5c;
@apply  font-fira_retina ;
}

#title {
  /*border: 1px solid #1E2D3D;*/
  color: #99abb9;
  background-color: #101920;
  border-radius: 0px;
  /*max-width: 400px; */
  /* max-height: 315px; */
}

#img {
  @apply flex justify-center w-full mt-5 h-80
}
#showcase {
  border-top-right-radius: 15px;
  border-top-left-radius: 15px;
}

#view-button {
  background-color: #1C2B3A;
}

#view-button:hover {
  background-color: #263B50;
}

#window {
  max-height: 120px;
  position: relative;
  overflow: hidden;
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
