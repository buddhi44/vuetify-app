<template>
  <v-app  class="grey lighten-4">
    
    <Navbar />

      
    <v-main>
      <router-view/>
    </v-main>

    <Footer />

    
  </v-app>
</template>

<script>
//import HelloWorld from './components/HelloWorld'
import Navbar from './components/Navbar'
import Footer from './components/footer'


export default {
  components: { Navbar,Footer },
  name: 'App',
  // components: {
  //   HelloWorld
  // },
  data () {
    return {
      //
    }
  }
}
</script>
