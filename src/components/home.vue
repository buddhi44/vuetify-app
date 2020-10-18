<template>
  <div >
    <h1>This is an Home page</h1>
     <div>
         <slider></slider>
          <card></card>
    </div>          
 </div>
</template>

<script>
import Slider from './Home/slider.vue'
import Card from './Home/card.vue'
  export default {

   components: { 'slider' : Slider,
                  'card'  : Card,
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
