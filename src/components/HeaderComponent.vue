<template>
  <div >
    <div class="header-style">
      <!-- header-top -->
        <div class="flex jc-between">
          <img alt="iAcademy-Logo" src="../../public/img/logo-light.png">
           <SliderMainComponent />
          <!-- navbar     -->
      
          <nav class="flex">
            <p><strong>HOME</strong></p>
            <p><strong>COURSES</strong></p>
            <p><strong>INSTRUCTORS</strong></p>
            <p><strong>EVENTS</strong></p>
            <p><strong>PAGES</strong></p>
            <p><strong>ELEMENTS</strong></p>
          </nav>
         
       
          <!-- icone     -->
          
          <div class="icon-container">
            <font-awesome-icon icon="fas fa-search" class="icon"/>
            <font-awesome-icon icon="fa-solid fa-bars" class="icon"/>
            <font-awesome-icon icon="fa-solid fa-cart-arrow-down" class="icon"/>
          </div>
        </div> 
        
      <!-- / header-top -->

      <!-- header-middle -->
      <div class="header-middle">
        <h1>Contemporary Ideas</h1>
        <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Adipisci dolore voluptate minima laboriosam ab iusto iste, officia nihil facere sint totam fugit officiis est.</p>
        <button><strong>REGISTER NOW</strong></button>
      </div>
      
    </div>
  </div>
</template>

<script>


// FONTAWESONE
  /* import the fontawesome core */
  import { library } from '@fortawesome/fontawesome-svg-core'

  /* import specific icons */
  import { faSearch } from '@fortawesome/free-solid-svg-icons'
  import { faBars } from '@fortawesome/free-solid-svg-icons'
  import { faCartArrowDown } from '@fortawesome/free-solid-svg-icons'

  /* import font awesome icon component */
  import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome'

  /* add icons to the library */
  library.add(faSearch, faBars, faCartArrowDown)

// FINE FONTAWESONE

import SliderMainComponent from '@/components/SliderMainComponent.vue'

export default {
  name: 'HeaderComponent',
  components: {
    FontAwesomeIcon,
    SliderMainComponent
  }
}
</script>


<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">



// inizio header-top
.header-style{
  height: 600px;
  // background-image: url("../../public/img/course-9-f-img.jpg");
  background-repeat: no-repeat;
  background-size: cover;
  //color: white;
  .jc-between {
    justify-content: space-between;
  }
}

img {
  height: 50px;
}

nav {
  padding: 10px;
  line-height: 50px;
  vertical-align: middle;
}

p {
  padding-left: 10px;
}

.icon-container{
  padding: 10px;
  line-height: 50px;
  vertical-align: middle;
}

.icon {
  padding: 10px;
}

// fine header-top


// inizio header-middle

.header-middle {
  margin: 150px;
  text-align: center;
  h1 {
    font-size: 70px;
    padding: 20px;
  }
  p {
    padding: 10px;
  }
  button {
  margin-top: 10px;
  background-color: #40c4ff;
  border: none;
  color: white;
  padding: 20px 40px;
  }
}



</style>
