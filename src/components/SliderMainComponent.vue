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
                  


                    <!-- <h2>{{slides[activeSlideIndex].title}}</h2>
                    <p>{{slides[activeSlideIndex].sottotitle}}</p>  -->
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
        }
    }
}
</script>

<style scoped>
.container {
    height: 600px;
    display: flex;
    justify-content: center;
    align-items: center;
}

.item {
    float: left;
    max-width: 1200px;
    /* height: 300px; */
    position: relative;
}

.item img {
   max-width: 1200px; 
    object-fit: contain;
    position: relative;
    opacity: 0.8;
}

.item .text {
    position: absolute;
    right: 20px;
    bottom: 20px;
    color: white;
}

.item h2 {
  position: absolute;
  top: 40%;
  left: 200px;
  font-size: 70px;
  color: white;
 
}

.item p {
  position: absolute;
  top: 50%;
  text-align: center;
  left: 10px;
  color: blue;
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