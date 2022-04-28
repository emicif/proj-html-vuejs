<template>
  <div>
      <div class="container" >
            <div class="slider-wrapper" tabindex="0" 
            @keyUp.down="showNextSlide" 
            @keyUp.up="showPrevSlide"
            @focus="startTimer"
            @mouseover="stopTimer"
            @mouseleave="startTimer"
            >

              <div class="item">
                <div class="card">
                  <img :src="slides[activeSlideIndex].image" :alt="slides[activeSlideIndex].title" /> 
                  <div class="flex first">
                    <h3>{{slides[activeSlideIndex].title}}</h3>  
                    <button>FREE</button>
                  </div>
                    <h5>{{slides[activeSlideIndex].sottotitle}}</h5>
                    <p>{{slides[activeSlideIndex].text}}</p>
                    <div class="flex bottom">
                      <div class="grey"><font-awesome-icon icon="fa-solid fa-user" /> 1 </div>
                     <div class="grey"><font-awesome-icon icon="fa-solid fa-bookmark" /> PROGRAMMING </div>
                    </div>
                     
                     
                  </div>
                   
                  <div class="card" v-if="activeSlideIndex<=11">
                    <img :src="slides[activeSlideIndex+1].image" :alt="slides[activeSlideIndex].title" /> 
                     <div class="flex first">
                      <h3>{{slides[activeSlideIndex+1].title}}</h3>  
                      <button>FREE</button>
                    </div>

                   
                    <h5>{{slides[activeSlideIndex+1].sottotitle}}</h5>
                    <p>{{slides[activeSlideIndex+1].text}}</p>
                      <div class="flex bottom">
                        <div class="grey"><font-awesome-icon icon="fa-solid fa-user" /> 1 </div>
                        <div class="grey"><font-awesome-icon icon="fa-solid fa-bookmark" /> PROGRAMMING </div>
                      </div>
                  </div> 


                  <div class="card" v-if="activeSlideIndex<=10">
                    <img :src="slides[activeSlideIndex+2].image" :alt="slides[activeSlideIndex].title" /> 
                    <div class="flex first second">
                      <h3>{{slides[activeSlideIndex+2].title}}</h3>  
                      <button>$20</button>
                    </div>
                     
                    <h5>{{slides[activeSlideIndex+2].sottotitle}}</h5>
                    <p>{{slides[activeSlideIndex+2].text}}</p>
                    <div class="flex bottom">
                      <div class="grey"><font-awesome-icon icon="fa-solid fa-user" /> 1 </div>
                     <div class="grey"><font-awesome-icon icon="fa-solid fa-bookmark" /> PROGRAMMING </div>
                    </div>
                  </div>  
                    
                </div>

                <div class="thumbs">
                    <div class="prev" v-show = "activeSlideIndex > 0" @click = "showPrevSlide" ></div>
                    <div class="next" v-show = "activeSlideIndex < slides.length - 3" @click = "showNextSlide" ></div>
                </div>

            </div>
               <ButtonComponent />
        </div>
  </div>
</template>



<script>

// FONTAWESONE
  /* import the fontawesome core */
  import { library } from '@fortawesome/fontawesome-svg-core'

  /* import specific icons */
  import { faUser } from '@fortawesome/free-solid-svg-icons'
  import { faBookmark } from '@fortawesome/free-solid-svg-icons'

  /* import font awesome icon component */
  import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome'

  /* add icons to the library */
  library.add(faUser, faBookmark)

// FINE FONTAWESONE

import ButtonComponent from '@/components/ButtonComponent.vue'

export default {
    name: 'CardComponent',
    components: {
    FontAwesomeIcon,
    ButtonComponent
    },
    data: function() {
      return {
        slides : [
        {
          image: 'img/course-1-f-img.jpg',
          title: "Android Developer",
          sottotitle: "David Sanders",
          text: "Lorem  ipsum dolor sit amet, te aeros consulatu pro, quem labores petentium no sea, atqui posidonium interpretaris"
        },
        {
          image: 'img/course-2-f-img.jpg',
          title: "Web Designing",
          sottotitle: "Jennifer Powell",
          text: "Lorem  ipsum dolor sit amet, te aeros consulatu pro, quem labores petentium no sea, atqui posidonium interpretaris"
        },
        {
          image: 'img/course-3-f-img.jpg',
          title: "Financial Modeling",
          sottotitle: "Edward Bowman",
          text: "Lorem  ipsum dolor sit amet, te aeros consulatu pro, quem labores petentium no sea, atqui posidonium interpretaris"

        },
        {
          image: 'img/course-4-f-img.jpg',
          title: "Financial Modeling",
          sottotitle: "Edward Bowman",
          text: "Lorem  ipsum dolor sit amet, te aeros consulatu pro, quem labores petentium no sea, atqui posidonium interpretaris"

        },
        {
          image: 'img/course-5-f-img.jpg',
          title: "Financial Modeling",
          sottotitle: "Edward Bowman",
          text: "Lorem  ipsum dolor sit amet, te aeros consulatu pro, quem labores petentium no sea, atqui posidonium interpretaris"

         
        },
        {
          image: 'img/course-6-f-img.jpg',
          title: "Course-6",
          sottotitle: "Edward Bowman",
          text: "Lorem  ipsum dolor sit amet, te aeros consulatu pro, quem labores petentium no sea, atqui posidonium interpretaris"
         
        },
        {
          image: 'img/course-7-f-img.jpg',
          title: "Course-7",
          sottotitle: "Edward Bowman",
          text: "Lorem  ipsum dolor sit amet, te aeros consulatu pro, quem labores petentium no sea, atqui posidonium interpretaris"
         
        },
        {
          image: 'img/course-8-f-img.jpg',
          title: "Course-8",
          sottotitle: "Edward Bowman",
          text: "Lorem  ipsum dolor sit amet, te aeros consulatu pro, quem labores petentium no sea, atqui posidonium interpretaris"
         
        },
        {
          image: 'img/course-9-f-img.jpg',
          title: "Course-9",
          sottotitle: "Edward Bowman",
          text: "Lorem  ipsum dolor sit amet, te aeros consulatu pro, quem labores petentium no sea, atqui posidonium interpretaris"
         
        },
        {
          image: 'img/course-10-f-img.jpg',
          title: "Course-10",
          sottotitle: "Edward Bowman",
          text: "Lorem  ipsum dolor sit amet, te aeros consulatu pro, quem labores petentium no sea, atqui posidonium interpretaris"
         
        },
        {
          image: 'img/course-11-f-img.jpg',
          title: "Course-11",
          sottotitle: "Edward Bowman",
          text: "Lorem  ipsum dolor sit amet, te aeros consulatu pro, quem labores petentium no sea, atqui posidonium interpretaris"
         
        },
        {
          image: 'img/course-12-f-img.jpg',
          title: "Course-12",
          sottotitle: "Edward Bowman",
          text: "Lorem  ipsum dolor sit amet, te aeros consulatu pro, quem labores petentium no sea, atqui posidonium interpretaris"
         
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
            this.intervalCleanerID = setInterval(this.showNextSlide - 3, 3000);
        },
        stopTimer(){
            clearInterval(this.intervalCleanerID);
        }
    }
}
</script>

<style scoped>
.container {
    height: 1000px;
    display: flex;
    justify-content: center;
    align-items: center;
    position: relative;
}

.item {
    display: flex;
    float: left;
    width: 100%;
    padding: 20px;
    max-width: 1200px;
    height: 00px;
    
 
}

.card {
  height: 500px;
  padding: 20px;
  background-color: white;
  border: 1px solid grey;
}

.first {
  padding-top: 20px;
  padding-bottom: 5px;
}



.card h5,
.card p {
  padding-bottom: 30px;
}


.item img {
   max-width: 1200px;
     width: 100%; 
    height: 200px; 
    object-fit: cover;
}

.item .text {
    position: absolute;
    right: 20px;
    bottom: 20px;
    text-align: right;
    color: white;
}

.thumbs {
    float: left;
    height: 850px;
    background: #000;
    position: relative;
   
}




.prev, .next {
    width: 20px;
    height: 20px;
    margin: 10px 0;
    border-radius: 50%;
    /* background: #ccc; */
    background: lightgray;
    position: absolute;
    right: 580px;
    bottom: 30%;
    cursor: pointer;
    z-index: 999;
}

.next {
  background: lightgray;
  position: absolute;
  right: 550px;
  bottom: 30%;
}


h5, .grey {
  color: grey;
}

p {
  color: rgb(89, 89, 89);
}


.grey {
  padding-right: 20px;
}
.bottom {
  margin-top: 10px;
}

.first {
  justify-content: space-between;
}

button {
  background-color: yellow;
  color: white;
  border: none;
  border-radius: 20%;
  padding: 0px 10px;

}

.second button {
  background-color: #55acee;
}

</style>