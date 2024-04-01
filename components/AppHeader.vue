<template>
     <header id="navbar" class="flex flex-col items-center bg-opacity-50">
      <div class="flex items-center mb-4" style="padding-top: 30px;">
        <div class="flex">
          <NuxtLink id="nav-logo" to="/">
            {{ config.dev.logo_name }}
            
          </NuxtLink>
        </div>
      </div>
      <nav class="flex w-full justify-center">
        <div class="flex">
          <NuxtLink id="nav-link" to="/" :class="{ active: isActive('/') }">
            <p>HOME</p>
          </NuxtLink>
          <NuxtLink id="nav-link" to="/RoomType" :class="{ active: isActive('/testab') }">
            <p>ROOMTYPE</p>
          </NuxtLink>
          <NuxtLink id="nav-link" to="/Gallery" :class="{ active: isActive('/_1') }">
            <p>GALLERY</p>
          </NuxtLink>
          <NuxtLink id="nav-link" to="/ContactUs" :class="{ active: isActive('/projects') }">
            <p>CONTACT US</p>
          </NuxtLink>
          <NuxtLink id="nav-link" to="/Promotion" :class="{ active: isActive('/projects') }">
            <p>PROMOTION</p>
          </NuxtLink>
          <NuxtLink id="nav-link" to="/QA" :class="{ active: isActive('/projects') }">
            <p>Q&A</p>
          </NuxtLink>
        </div>
      </nav>
  </header>
</template>

<style>
#navbar > nav {
  width: fit-content;
  height: 25px;
  font-size: 13px;
}

#nav-link {

  color: gray;
  @apply  text-brown-text font-fira_retina px-6 h-full flex items-center ;
}

#nav-link-contact {

  font-weight: 100;
  @apply text-menu-text font-fira_retina px-6 h-full flex items-center;
}

#nav-link:hover, #nav-link-contact:hover p{
  font-weight: 850;
  
}

#nav-logo {
  margin: auto 0;
  font-weight: 100;
  @apply text-menu-text font-fira_retina h-full flex items-center;
}

#nav-logo:hover {
  font-weight: 850;
  
}

#nav-link.router-link-active p{
  border-bottom: 1px solid #484642;
  border-top: 1px solid #484642;
  font-weight: 850;
}

#nav-logo.router-link-active {
  border-right: 0px solid #746c5c;
  border-bottom: none;
  color: white;
  @apply text-brown-text;
}

</style>

<script>

export default {
  computed: {
    // Set active class to current page link
    isActive() {
      return route => this.$route.path === route;
    }
  },
  setup() {
    const config = useRuntimeConfig()

    return {
      config
    }
  },
};

</script>
