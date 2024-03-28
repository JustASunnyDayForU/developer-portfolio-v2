<template>
     <header id="navbar" class="flex flex-col items-center">
    <div class="flex items-center mb-4">
      <div class="flex">
        <NuxtLink id="nav-logo" to="/">
          {{ config.dev.logo_name }}
        </NuxtLink>
      </div>
    </div>
    <nav class="w-full flex justify-center border-t border-b lg:border-none">
      <div class="flex">
        <NuxtLink id="nav-link" to="/" :class="{ active: isActive('/') }">
          HOME
        </NuxtLink>
        <NuxtLink id="nav-link" to="/RoomType" :class="{ active: isActive('/testab') }">
          ROOMTYPE
        </NuxtLink>
        <NuxtLink id="nav-link" to="/Gallery" :class="{ active: isActive('/_1') }">
          GALLERY
        </NuxtLink>
        <NuxtLink id="nav-link" to="/ContactUs" :class="{ active: isActive('/projects') }">
          CONTACT US
        </NuxtLink>
        <NuxtLink id="nav-link" to="/Promotion" :class="{ active: isActive('/projects') }">
          PROMOTION
        </NuxtLink>
        <NuxtLink id="nav-link" to="/QA" :class="{ active: isActive('/projects') }">
          Q&A
        </NuxtLink>
      </div>
    </nav>
  </header>
</template>

<style>

#nav-link {
  border-right: 1px solid #746c5c;
  color: white;
  @apply  text-brown-text font-fira_retina px-6 h-full flex items-center ;
}

#nav-link-contact {
  border-left: 1px solid #746c5c;
  @apply text-menu-text font-fira_retina px-6 h-full flex items-center;
}

#nav-link:hover, #nav-link-contact:hover {
  background-color: #746c5c;
  color: white;
}

#nav-logo {
  border-right: 1px solid #746c5c;
  @apply text-brown-text font-fira_retina px-16 h-full flex items-center;
}

#nav-logo:hover {
  background-color: white;
  color: #746c5c;
}

#nav-link.router-link-active, #nav-link-contact.router-link-active {
  border-bottom: 2px solid #746c5c;
  border-top: 2px solid #746c5c;
  border-right: 2px solid #746c5c;
  color: #746c5c;
  
}

#nav-link.router-link-active:hover{
  color: white;
}

#nav-logo.router-link-active {
  border-right: 0px solid #746c5c;
  border-bottom: none;
  color: white;
  @apply text-brown-text;
}

#navbar > nav {
  height: 45px;
  font-size: 13px;
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
