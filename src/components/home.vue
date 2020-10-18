<template>
  
    
     <div>
            <slider></slider>
            <div  class="container">
                  <div class="row">
                      <div class="col 12">
                        <section1></section1>
                      </div>
                      
                  </div>


                  <div class="row">
                    <div class="col 12">
                       <card></card>
                    </div>
                  </div>
                  

                   <div class="row">
                      <div class="col 12">
                        <section2></section2>
                      </div>
                    </div>

                   <div class="row">
                      <div class="col 12">
                        <section3></section3>
                      </div>
                  </div>
                 
            </div>
    </div>          
 
</template>

<script>
import Slider from './Home/slider.vue'
import Card from './Home/card.vue'
import Section1 from './Home/section1.vue'
import Section2 from './Home/section2.vue'
import Section3 from './Home/section3.vue'

  export default {

   components: { 'slider' : Slider,
                  'card'  : Card,
                  'section1':Section1,
                   'section2':Section2,
                    'section3':Section3,
            },
  
    data: () => ({
      model: 'caption',
      sizes: [
        ['mdi-devices', 'all', 'caption'],
        ['mdi-cellphone-iphone', 'sm', 'body-2'],
        ['mdi-laptop', 'md', 'body-1'],
        ['mdi-monitor', 'lg', 'h6'],
        ['mdi-television', 'xl', 'h4'],
      ],
    }),

    computed: {
      typeClass () {
        const type = ['text', this.model]
        const [, breakpoint] = this.current

        if (breakpoint !== 'all') {
          type.splice(1, 0, breakpoint)
        }

        return `.${type.join('-')}`
      },
      current () {
        return this.sizes.find(size => size[2] === this.model)
      },
    },
  }
</script>


