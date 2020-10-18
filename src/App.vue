<template>

  <div >
       <v-app >
    
        <Navbar />

      
        <v-main>
              <router-view/>
        </v-main>

        <Footer />

    
         </v-app>

  </div>
 
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
