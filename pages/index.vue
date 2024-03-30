<template>
  	<main v-if="!loading">

      <section class="content">

        <div id="info">
          <div class="head">
            <span>
              Hi all, I am
            </span>
            <h1>{{ config.dev.name }}</h1>
            <h2>> {{ config.dev.role }}</h2>
          </div>
          
        </div>
      </section>

	</main>
</template>

<style>

main {

}

.content {
  display: flex;
  flex-direction: column;
  height: 100%;
  width: 100%;
  overflow: hidden;
	justify-content: center;
	
}

.head {
  padding-bottom: 3rem;
}

#info {
  width: 100%;
	display: flex;
	flex-direction: column;
}

#info > span {
  font-size: 14px;
  line-height: 1;
  color: #607B96;
  font-family: 'Fira Code Retina';
  padding-bottom: 1rem;
}

#info {
	padding-block: 2.5rem;
}

.hide {
  display: none;
}


/* mobile */
@media (max-width: 768px) {
	main .content {
		display: flex;
		flex-direction: column;
		justify-content: space-between;
		margin: 1.75rem; /* 28px */
	}

}

</style>

<script>
export default {
  name: 'Hello',
  setup() {
    const config = useRuntimeConfig()
    return {
      config
    }
  },
  data() {
    return {
      isMobile: false,
      loading: true
    }
  },
  mounted() {
    // Detectamos si es mobile
    if (window.innerWidth <= 1024) {
      this.isMobile = true
    }

    // Escuchamos los cambios de tamaño de pantalla
    window.addEventListener('resize', this.handleResize)

    // When the component is mounted, we can remove the loader.
    this.loading = false
  },
  beforeDestroy() {
    // Remove the event listener when the component is destroyed.
    window.removeEventListener('resize', this.handleResize)
  },
  methods: {
    handleResize() {
      if (window.innerWidth <= 1024) {
        this.isMobile = true
      } else {
        this.isMobile = false
      }
    }
  }
}
</script>

