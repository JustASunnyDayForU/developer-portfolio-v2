<template>
  <main id="contact-me" class="page">
    
    <div class="flex-col w-full overflow-auto">

        <div class="flex justify-end">
            <div id="header" class="text-right pr-24 w-72">
                ZOOM-IN MAP
            </div>
        </div>
        <div id="img">
              <img src="/images/projects/ai-resources.png" alt="">
          </div>

          <div class="flex flex-col items-center relative p-6">
            <span class="bg-slate-500 w-full h-32 absolute top-20 left-0"></span>
            <div class="flex justify-center z-10">
                <img src="/images/projects/ai-resources.png" alt="" class="max-h-80">
            </div>
            </div>

        <!-- windows tab -->
        <div class="tab-height w-full hidden lg:flex border-right border-bot items-center">

            <!-- main -->
            <div class="flex lg:grid lg:grid-cols-2 h-full w-full">
      
                <div id="left" class="h-full w-full flex flex-col border-right items-center">
                    <ContactForm :name="name" :email="email" :message="message" />

                </div>

                <div id="right" class="h-full w-full hidden lg:flex">
                  

                    <!-- scroll bar -->
                    <div id="scroll-bar" class="h-full border-left flex justify-center py-1">
                        <div id="scroll"></div>
                    </div>
              
                </div>
            </div>
        </div>

    </div>
  </main>
</template>

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

<style>

#img {
  @apply flex justify-center w-full mt-5 h-80
}

.form-content {
  padding: 75px 50px 0px 75px;
  width: 100%;
  height: 100%;
  overflow-y: auto;
  font-size: 15px;
}
#header {
  min-width: 500px;
  margin-bottom: 5px;
  color: #746c5c;
@apply  font-fira_retina;
}

</style>