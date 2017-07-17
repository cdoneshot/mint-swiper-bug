<template>
  <Swipe class="swipe-container" :continuous="true">
    <SwipeItem v-for="image in images" :key="image.index">
      <img :src="image.src">
    </SwipeItem>
  </Swipe>
</template>

<script>
  import {Swipe, SwipeItem} from 'mint-ui'
  import 'mint-ui/lib/style.css'

  import img1 from '~assets/1.jpeg'
  import img2 from '~assets/2.jpg'
  export default {
    asyncData(){
      return {
        images: [
          {src: img1, index: 1},
          {src: img2, index: 2}]
      }
    },
    components: {
      Swipe,
      SwipeItem
    }
  }
</script>

<style>
  .swipe-container {
    width: 200px;
    height: 200px;
  }

  .swipe-container img {
    width: 100%;
    height: 100%;
  }
</style>
