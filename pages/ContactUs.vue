<script>
export default {
  data() {
      return {
          name: '',
          email: '',
          message: '',
      }
  },
  setup() {
      const contact = useRuntimeConfig().dev.contacts

      return {
          contact
      }
  },
  methods: {
      open(elementId) {
          const element = document.getElementById(elementId);
          const arrow = element.querySelector('.arrow');
          const links = element.querySelector('#links');

          if (links.style.display === 'block') {
              links.style.display = 'none';
              arrow.style.transform = 'rotate(0deg)';
          } else {
              links.style.display = 'block';
              arrow.style.transform = 'rotate(90deg)';
          }
      }
  },
}

</script>

<template>
  <main id="contact-me" class="page">
    
    <div class="section">
        <div class="text-xl" style="text-align: end; padding-right: 20px;">
            LOCATION
        </div>
        <img src="/images/projects/ai-resources.png" alt="" style="width: 100%; height: fit-content; object-fit: contain;">
  
    </div>
    <div class="section">
        <div style="display: flex; flex-direction: column; justify-content: center; align-items: center; margin: 0; min-height: fit-content; width: 100%; height: 40vw;">
            <img src="/images/projects/ai-resources.png" alt="" style="width: 50%; position: absolute; object-fit: contain;">
            <div style="background-color: white; width: 100%; height: 25%;">
                
            </div>
            <div style="background-color: #d3d3d3; width: 100%; height: 50%;">
                
            </div>
            <div style="background-color: white; width: 100%; height: 25%;">
                
            </div>
        </div>
    </div>

  </main>
</template>

<style scoped>


</style>