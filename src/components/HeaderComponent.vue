<template>
  <div>

      <div class="header-style">
        <div class="container">
            <div class="slider-wrapper" tabindex="0" 
            @keyUp.down="showNextSlide" 
            @keyUp.up="showPrevSlide"
            @focus="startTimer"
            @mouseover="stopTimer"
            @mouseleave="startTimer"
            >
                <div class="slideImage" :style="setBackgroundImage">
                     <div class="flex jc-between white">

                          <img class="logo" alt="iAcademy-Logo" src="../../public/img/logo-light.png">
                          <nav class="flex">
                            <p><strong>HOME</strong></p>
                            <p><strong>COURSES</strong></p>
                            <p><strong>INSTRUCTORS</strong></p>
                            <p><strong>EVENTS</strong></p>
                            <p><strong>PAGES</strong></p>
                            <p><strong>ELEMENTS</strong></p>
                          </nav>
                          
                          <div class="icon-container">
                            <font-awesome-icon icon="fas fa-search" class="icon"/>
                            <font-awesome-icon icon="fa-solid fa-bars" class="icon"/>
                            <font-awesome-icon icon="fa-solid fa-cart-arrow-down" class="icon"/>
                          </div>
                      </div>  
                        <div class="text">
                          <h2>{{slides[activeSlideIndex].title}}</h2>
                          <p>{{slides[activeSlideIndex].sottotitle}}</p> 
                        </div>  
                        
                </div>
                <!-- fine slider -->
                 <div class="thumbs">
                      <div class="prev" v-show = "activeSlideIndex > 0" @click = "showPrevSlide" ></div>
                      <div class="next" v-show = "activeSlideIndex < slides.length - 1" @click = "showNextSlide" ></div>
                  </div> 
              </div>
        </div>
     </div>     
        
            
                <!-- <div class="item">
                    <img :src="slides[activeSlideIndex].image" :alt="slides[activeSlideIndex].title" />  -->
                    
                  

                
                 
               


     
      
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


export default {
  name: 'HeaderComponent',
  components: {
    FontAwesomeIcon,
  },
   data: function() {
      return {
        slides : [
        {
          id: 0,
          image: 'img/course-1-f-img.jpg',
          title: "Contemporary Ideas",
          sottotitle: "Lorem ipsum dolor sit amet consectetur, adipisicing elit. Adipisci dolore voluptate minima laboriosam ab iusto iste, officia nihil facere sint totam fugit officiis est."
        },
        {
          image: 'img/course-2-f-img.jpg',
          title: "Course-2",
          sottotitle: "Lorem ipsum dolor sit amet consectetur, adipisicing elit. Adipisci dolore voluptate minima laboriosam ab iusto iste, officia nihil facere sint totam fugit officiis est."

        },
        {
          image: 'img/course-3-f-img.jpg',
          title: "Course-3",
          sottotitle: "Lorem ipsum dolor sit amet consectetur, adipisicing elit. Adipisci dolore voluptate minima laboriosam ab iusto iste, officia nihil facere sint totam fugit officiis est."
        },
        {
          image: 'img/course-4-f-img.jpg',
          title: "Course-4",
          sottotitle: "Lorem ipsum dolor sit amet consectetur, adipisicing elit. Adipisci dolore voluptate minima laboriosam ab iusto iste, officia nihil facere sint totam fugit officiis est."
        },
        {
          image: 'img/course-5-f-img.jpg',
          title: "Course-5",
          sottotitle: "Lorem ipsum dolor sit amet consectetur, adipisicing elit. Adipisci dolore voluptate minima laboriosam ab iusto iste, officia nihil facere sint totam fugit officiis est."
        },
        {
          image: 'img/course-6-f-img.jpg',
          title: "Specialized Training",
          sottotitle: "Lorem ipsum dolor sit amet consectetur, adipisicing elit. Adipisci dolore voluptate minima laboriosam ab iusto iste, officia nihil facere sint totam fugit officiis est."
        },
        {
          image: 'img/course-7-f-img.jpg',
          title: "Course-7",
          sottotitle: "Lorem ipsum dolor sit amet consectetur, adipisicing elit. Adipisci dolore voluptate minima laboriosam ab iusto iste, officia nihil facere sint totam fugit officiis est."
        },
        {
          image: 'img/course-8-f-img.jpg',
          title: "Course-8",
          sottotitle: "Lorem ipsum dolor sit amet consectetur, adipisicing elit. Adipisci dolore voluptate minima laboriosam ab iusto iste, officia nihil facere sint totam fugit officiis est."
        },
        {
          image: 'img/course-9-f-img.jpg',
          title: "Contemporary Ideas",
          sottotitle: "Lorem ipsum dolor sit amet consectetur, adipisicing elit. Adipisci dolore voluptate minima laboriosam ab iusto iste, officia nihil facere sint totam fugit officiis est."
        }
      ],
      activeSlideIndex: 0,
      intervalCleanerID: undefined,

      }   
   },
   methods: {
        showPrevSlide(){
            if (this.activeSlideIndex > 0) {
                this.activeSlideIndex --;
            }
        },
        showNextSlide(){
            if (this.activeSlideIndex < this.slides.length -1) {
                this.activeSlideIndex ++;
            }
        },
        startTimer(){
            this.intervalCleanerID = setInterval(this.showNextSlide, 3000);
        },
        stopTimer(){
            clearInterval(this.intervalCleanerID);
        },
        
   },
   computed: {
      setBackgroundImage(){
      return {backgroundImage : "url(" +this.slides[this.activeSlideIndex].image+ ")"}
      }
    }
}
</script>


<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">



// inizio header-top
.header-style{
  background-repeat: no-repeat;
  background-size: cover;
}

.jc-between {
    justify-content: space-between;
}

.white {
  color: white;
}

.logo {
  height: 50px;
  margin: 10px;
}

nav {
  padding: 10px;
  line-height: 50px;
  vertical-align: middle;
}

nav p:hover {
 color: #40c4ff;
}

p {
  padding-left: 10px;
}

.icon-container{
  margin: 10px;
}

.icon {
  margin: 10px;
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

// slide

.container {
    width: 100%;
    height: 100vh;
    max-width: 1200px;


}

.item {
    float: left;
    max-width: 1200px;
    /* height: 300px; */
    // position: relative;
}

.item img {
   max-width: 1200px; 
    object-fit: contain;
  
    opacity: 0.8;
}

.item .text {
    position: absolute;
    right: 20px;
    bottom: 20px;
    color: white;
}

.text h2 {
  text-align: center;
  font-size: 70px;
  color: white;
  padding-top: 300px;

}

.text p {
  padding-top: 20px;
}

p {
  text-align: center;
  color: white;
 
}

.thumbs {
    float: left;
    height: 300px;
    background: #000;
    position: relative;
  
}

.thumb {
    height: calc((300px) / 5);
    opacity: 0.5;
}

.thumb img {
    width: 100%;
    height: 100%;

}

.thumb.active {
    border: 2px solid #ccc;
    opacity: 1;
}

.prev, .next {
    width: 20px;
    height: 20px;
    margin: 10px 0;
    border-radius: 50%;
    /* background: #ccc; */
    background: red;
    position: absolute;
    cursor: pointer;
    z-index: 999;
}

.prev {
  background: lightgray;
  top: -20%;
  left: 600px;
}

.next {
  background: lightgray;
  top: -20%;
  left: 650px;
}


//slider
.slideImage {
  width: 100%;
  height: 100vh;
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  // background-image: url("/public/img/course-1-f-img.jpg")
  position: relative;
}



</style>
