<template>
  <div class="container">
     <div class="flex">
      <img src="../../public/img/h5-img-2.jpg" alt="">
      <div class="box-right">
        <h2>Empowering Children to Reach Their Potential.</h2>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Veniam eius molestiae nulla assumenda ad tempore accusantium totam nam, sunt, mollitia veritatis, distinctio ipsam fugit labore omnis deserunt quibusdam excepturi maxime.</p>
      <div class="flex numberText">
        <div class="pr100">
          <p class="number">168</p>
          <p>User Stories</p>
        </div>
        <div>
          <p class="number">347</p>
          <p>Events</p>
        </div>
        
      </div>
      <div class="button">
          <ButtonComponent />
        </div> 
      </div>
    </div>
  </div>
</template>

<script>

import ButtonComponent from '@/components/ButtonComponent.vue'


export default {
    name: 'ChildrenComponent',
    components: {
      ButtonComponent
    }
  }
</script>

<style scoped lang="scss">

.container {
  margin-top: 50px;

  img {
  width: 50%;
  }
  .box-right {
    width: 500px;
  }
  h2 {
    font-size: 2.5rem;
    padding-bottom: 20px;
  }
  .numberText {
    color: #40C4FF;
    font-size: 1rem;
    padding-top: 40px;  
  }
  .number {
    font-size: 2.5rem;
  }
  .pr100 {
    padding-right: 100px;
  }
 
}




</style>