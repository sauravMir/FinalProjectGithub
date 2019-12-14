<template>
  <div>
    <header-nav></header-nav>
    <section class="main-content columns">
      <div class="container column is-10">
        <section class="section">  
          
        <nuxt />
      </section>
        
      </div>
    </section>
  </div>
</template>

<script>
import Header from '.././components/Header'
export default {
  data () {
    return {
      items: [
        {
          title: 'Home',
          icon: 'home',
          to: { name: 'index' }
        },
        {
          title: 'Inspire',
          icon: 'lightbulb',
          to: { name: 'inspire' }
        }
      ]
    }
  },
  components: {
    headerNav : Header
  },
}
</script>
