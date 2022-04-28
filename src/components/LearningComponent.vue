<template>
  <div>
      <div class="container" >
            <div class="slider-wrapper" tabindex="0" 
              @keyUp.down="showNextSlide" 
              @keyUp.up="showPrevSlide"
              >

             <div class="thumbs">
               <div class="thumb" v-for="(slide, index) in slides" :key="slide.id" @click="setActive(index)" :class="{ active: isActive }" >
                 
                  <h3>{{slide.titlethumbs}}</h3>
                
               </div>
                
              </div>

              
              <div class="item">
                <h3>{{slides[activeSlideIndex].title}}</h3>
                <p class="pt20">{{slides[activeSlideIndex].text}}</p>

                <div class="flex pt40 card-inside">
                  <div class="elenco">     
                    <p><font-awesome-icon class="icon" icon="fa-solid fa-check" /> {{slides[activeSlideIndex].sottotitle}}</p>
                    <p><font-awesome-icon class="icon" icon="fa-solid fa-check" /> {{slides[activeSlideIndex].sottotitle_2}}</p>
                    <p><font-awesome-icon class="icon" icon="fa-solid fa-check" /> {{slides[activeSlideIndex].sottotitle_3}}</p>
                    <p><font-awesome-icon class="icon" icon="fa-solid fa-check" /> {{slides[activeSlideIndex].sottotitle_4}}</p>
                  </div>
                      
                  <img :src="slides[activeSlideIndex].image" :alt="slides[activeSlideIndex].title" />
                </div>
              </div>

            </div>
      </div>
  </div>
</template>

<script>

// FONTAWESONE
  /* import the fontawesome core */
  import { library } from '@fortawesome/fontawesome-svg-core'

  /* import specific icons */
  import { faCheck } from '@fortawesome/free-solid-svg-icons'


  /* import font awesome icon component */
  import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome'

  /* add icons to the library */
  library.add(faCheck)

// FINE FONTAWESONE


export default {
    name: 'LearningComponent',
    components: {
    FontAwesomeIcon,
    },
    data: function() {
      return {
        slides : [
        {
          titlethumbs: "What We Do",
          title: "Learning Possibilities",
          text: "Lorem  ipsum dolor sit amet, te aeros consulatu pro, quem labores petentium no sea, atqui posidonium interpretaris",
          sottotitle: "We wneich lives thwough learning.",
          sottotitle_2: "Maximizing potential through individual attention.",
          sottotitle_3: "The trusted name for specialized training",
          sottotitle_4: "People teach. People learn. This is where they connect",
          image: 'img/h12-tabs-icon-1.png',
        },
        {
          titlethumbs: "Degree Programme",
          title: "Programme",
          text: "Lorem  ipsum dolor sit amet, te aeros consulatu pro, quem labores petentium no sea, atqui posidonium interpretaris",
          sottotitle: "We wneich lives thwough learning.",
          sottotitle_2: "Maximizing potential through individual attention.",
          sottotitle_3: "The trusted name for specialized training",
          sottotitle_4: "People teach. People learn. This is where they connect",
          image: 'img/h12-tabs-icon-2.png',
        },
        {
          titlethumbs: "Career Achievements",
          title: "Career",
          text: "Lorem  ipsum dolor sit amet, te aeros consulatu pro, quem labores petentium no sea, atqui posidonium interpretaris",
          sottotitle: "We wneich lives thwough learning.",
          sottotitle_2: "Maximizing potential through individual attention.",
          sottotitle_3: "The trusted name for specialized training",
          sottotitle_4: "People teach. People learn. This is where they connect",
          image: 'img/h12-tabs-icon-3.png',
        },
        {
          titlethumbs: "Personal Managment",
          title: "Your Personal Managment",
          text: "Lorem  ipsum dolor sit amet, te aeros consulatu pro, quem labores petentium no sea, atqui posidonium interpretaris",
          sottotitle: "We wneich lives thwough learning.",
          sottotitle_2: "Maximizing potential through individual attention.",
          sottotitle_3: "The trusted name for specialized training",
          sottotitle_4: "People teach. People learn. This is where they connect",
          image: 'img/h12-tabs-icon-4.png',
        },
        {
          titlethumbs: "Steps To Success",
          title: "Steps To Success",
          text: "Lorem  ipsum dolor sit amet, te aeros consulatu pro, quem labores petentium no sea, atqui posidonium interpretaris",
          sottotitle: "We wneich lives thwough learning.",
          sottotitle_2: "Maximizing potential through individual attention.",
          sottotitle_3: "The trusted name for specialized training",
          sottotitle_4: "People teach. People learn. This is where they connect",
          image: 'img/h12-tabs-icon-5.png',
        },
        {
          titlethumbs: "Knowledge Trans",
          title: "Knowledge",
          text: "Lorem  ipsum dolor sit amet, te aeros consulatu pro, quem labores petentium no sea, atqui posidonium interpretaris",
          sottotitle: "We wneich lives thwough learning.",
          sottotitle_2: "Maximizing potential through individual attention.",
          sottotitle_3: "The trusted name for specialized training",
          sottotitle_4: "People teach. People learn. This is where they connect",
          image: 'img/h12-tabs-icon-6.png',
        }
      ],
      activeSlideIndex: 0,
      isActive: false
      }
    },
    methods: {
        setActive: function (i) {
          this.activeSlideIndex = i;
          return this.isActive = true 
        }
    }
}
</script>

<style scoped>

/* utilities */

.pt20 {
  padding-top: 20px
}


.pt40 {
  padding-top: 40px
}


.container {
    height: 600px;
    display: flex;
    justify-content: center;
    align-items: center;
}

.item {
    float: left;
    width: 700px;
    height: 300px;
    padding: 30px;
}

.item img {
    width: 20%;
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
    width: 150px;
    height: 400px;
    border: 1px solid lightgray;
    position: relative;
}

.thumb {
  height: calc((400px) / 6);
  opacity: 1;
  border-bottom: 1px solid lightgray;
}

.thumb img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

/* .thumb:active {
  border-left: 2px solid rgb(210, 13, 13);
  opacity: 2;
} */

.active {
  border-left: 2px solid rgb(210, 13, 13);
}

.card-inside {
  justify-content: space-between;
}



.item h3 {
  font-size: 40px;
}

.item p {
  font-size: 20px;
  color: grey;
}

.elenco {
  padding-top: 20px;
}

.elenco p {
  padding-bottom: 10px;
}

.icon {
  color: #55acee;
}

</style>