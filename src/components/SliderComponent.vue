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
              <img :src="slides[activeSlideIndex].image" :alt="slides[activeSlideIndex].title" /> 
              <p>{{slides[activeSlideIndex].text}}</p>
              <h3>{{slides[activeSlideIndex].title}}</h3>  
              <h5>{{slides[activeSlideIndex].sottotitle}}</h5>
              
              
                <div class="thumbs">
                    <div class="prev" v-show = "activeSlideIndex > 0" @click = "showPrevSlide" ></div>
                    <div class="next" v-show = "activeSlideIndex < slides.length - 1" @click = "showNextSlide" ></div>
                </div>

            </div>
        </div>
  </div>
</template>



<script>
export default {
    name: 'SliderComponent',
    data: function() {
      return {
        slides : [
        {
          image: 'img/testimonials-standard-1.png',
          title: "Joan Collins",
          sottotitle: "STUDENT",
          text: "Lorem  ipsum dolor sit amet, te aeros consulatu pro, quem labores petentium no sea, atqui posidonium interpretaris. "

        },
        {
          image: 'img/testimonials-standard-2.png',
          title: "Android Developer",
          sottotitle: "STUDENT",
          text: "Lorem  ipsum dolor sit amet, te aeros consulatu pro, quem labores petentium no sea, atqui posidonium interpretaris"
        },
        {
          image: 'img/testimonials-standard-3.png',
          title: "Android Developer",
          sottotitle: "STUDENT",
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
            this.intervalCleanerID = setInterval(this.showNextSlide, 3000);
        },
        stopTimer(){
            clearInterval(this.intervalCleanerID);
        }
    }
}
</script>

<style scoped>
.container {
    height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
    background-image: url('../../public/img/h5-parallax-img-1.png');
    background-repeat: no-repeat;
    background-size: cover;
    text-align: center;
    color: white;
    margin-top: 30px;
    
}

.item {
    float: left;
    width: 700px;
    max-width: 1200px;
    height: 300px;
    position: absolute;
    

}

.item img {
   max-width: 1200px;
     width: 100%; 
    height: 100%; 
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
    height: 300px;
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
    position: relative;
    top: 50%;
    left: 440px;
   
    cursor: pointer;
    z-index: 999;
}

.prev {
   background: red;
  transform: translate(-50%);
}

.next {
  background: yellow;
  transform: translate(-50%);
}


/* custom */
img {
  padding-bottom: 30px;
}

p {
   padding-bottom: 50px;
}

h3 {
  padding-bottom: 10px; 
}

</style>