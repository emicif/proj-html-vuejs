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
                    <img :src="slides[activeSlideIndex].image" :alt="slides[activeSlideIndex].title" /> 
                        
                </div>

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
    name: 'SliderMainComponent',
    data: function() {
      return {
        slides : [
        {
          image: 'img/course-1-f-img.jpg',
          title: "Course-1"
        },
        {
          image: 'img/course-2-f-img.jpg',
          title: "Course-2"
        },
        {
          image: 'img/course-3-f-img.jpg',
          title: "Course-3"
         
        },
        {
          image: 'img/course-4-f-img.jpg',
          title: "Course-4"
         
        },
        {
          image: 'img/course-5-f-img.jpg',
          title: "Course-5"
         
        },
        {
          image: 'img/course-6-f-img.jpg',
          title: "Course-6"
         
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
}

.item {
    float: left;
    width: 700px;
    max-width: 1200px;
    height: 300px;
    position: relative;
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
    top: 50%;
    left: 0px;
    transform: translate(-2000%);
    cursor: pointer;
    z-index: 999;
}

.next {
  background: yellow;
  transform: translate(-1800%);
}

</style>