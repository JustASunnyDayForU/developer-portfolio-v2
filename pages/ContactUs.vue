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
  mounted(){

      const nameInput = document.getElementById('name-input');
      const emailInput = document.getElementById('email-input');
      const messageInput = document.getElementById('message-input');

      nameInput.addEventListener('input', (event) => {
          const nameValue = document.getElementById('name-value')
          nameValue.innerHTML = event.target.value;
      })

      emailInput.addEventListener('input', (event) => {
          const emailValue = document.getElementById('email-value')
          emailValue.innerHTML = event.target.value;
      })

      messageInput.addEventListener('input', (event) => {
          const messageValue = document.getElementById('message-value')
          messageValue.innerHTML = event.target.value;
      })

      /**
       * * Close all submenus
       * ! This is a temporary solution.
       * ! This is needed because when the page is loaded, height style on #links are not applied.
       */
      const links = document.getElementsByClassName('submenu');
      for (let i = 0; i < links.length; i++) {
          if(window.innerWidth > 1024){ 
              links[i].querySelector("#links").style.display = "block";
              links[i].querySelector(".arrow").style.transform = "rotate(90deg)";
          } else {
              links[i].querySelector("#links").style.display = "none";
          }
      }
  },
}

</script>

<template>
  <main id="contact-me" class="page">
    
    <div class="section">
        <div style="width: 100%; height: 70px; 
            background: rgb(124,124,124);  
            background: linear-gradient(90deg, rgba(124,124,124,1) 0%, rgba(135,135,135,1) 60.5%, rgba(255,255,255,1) 60.5%, rgba(251,251,251,1) 61%, rgba(213,213,213,1) 61%, rgba(194,194,194,1) 100%);
            text-align: start; align-items: center;">
            <div id="title" class="text-3xl">
                LOCATION
            </div>
        </div>
        <div id="img">
              <img src="/images/projects/ai-resources.png" alt="">
        </div>

        <div class="section">
            <div style="width: 100%; height: 70px; 
            background: rgb(124,124,124);  
            background: linear-gradient(90deg, rgba(124,124,124,1) 0%, rgba(135,135,135,1) 60.5%, rgba(255,255,255,1) 60.5%, rgba(251,251,251,1) 61%, rgba(213,213,213,1) 61%, rgba(194,194,194,1) 100%);
            text-align: start;">
                <div id="title" class="text-3xl flex">
                    CONTACT US
                </div>
            </div>
            <div class="flex lg:grid lg:grid-cols-2 h-full w-full" style="padding: 10px;">
      
                <div id="left" class="h-full w-full flex flex-col border-right items-center">
                    

                </div>

                <div id="right" class="h-full w-full hidden lg:flex" style="justify-content: center;">
                    <ContactForm :name="name" :email="email" :message="message" />

                </div>
            </div>
        </div>

    </div>
  </main>
</template>

<style scoped>


#img {
  @apply flex justify-center w-full mt-5 h-80
}

#header {
  
  
}

</style>