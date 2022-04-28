<template>
  <div>
    <div class="container">
      <div class="title">
        <h2>Princing Plans</h2>
        <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Ipsa, placeat nulla? Quod tenetur alias quas, veritatis officiis nostrum necessitatibus minima</p>
      </div>

       
      
      <!-- table -->
      <div class="flex clearfix col-container">
            <!-- prima colonna --> 
            
                    <div class="first-part-col col">
                        <div class="title-col-first">
                          <h3><strong>Save up to 40% by paying weekly</strong></h3>
                        </div>
                        

                            <div class="second-col-title">
                                <ul>
                                    <li>Number of Courses</li>
                                    <li>Time</li>
                                    <li>Web Designing</li>
                                    <li>Human-Centered Design</li>
                                    <li>Basic Marketing</li>
                                    <li>Python for Everybody</li>
                                    <li>Android Developer</li>
                                    <li>Business English</li>
                                </ul>
                            </div> 
                    </div>            
                

        
              <!-- seconda colonna -->
              <div class="col colomn">
                <div class="title-col">
                  <img src="img/h5-custom-icon-7.png" alt="">
                  <h3><strong>Standard</strong></h3>
                  <p><strong>$12</strong></p>
                </div>
                  <div>
                      <ul>
                          <li>2</li>
                          <li>15 Days</li>
                          <li class="flag"><font-awesome-icon icon="fa-solid fa-check" /></li>
                          <li class="flag"><font-awesome-icon icon="fa-solid fa-check" /></li>
                          <li><font-awesome-icon icon="fa-solid fa-xmark" /></li>
                          <li><font-awesome-icon icon="fa-solid fa-xmark" /></li>
                          <li><font-awesome-icon icon="fa-solid fa-xmark" /></li>
                          <li><font-awesome-icon icon="fa-solid fa-xmark" /></li>
                      </ul>
                      <div class="button"><button>GET IT NOW</button></div>
                  </div> 
              </div>


                <!-- terza colonna -->
                <div class="col colomn border-top-blue">
                    <div class="title-col-2">
                      <img src="img/h5-custom-icon-8.png" alt="">
                      <h3><strong>Professional</strong></h3>
                      <p><strong>$12</strong></p>
                    </div>
                    <div>
                      <ul>
                          <li>4</li>
                          <li>30 Days</li>
                          <li class="flag"><font-awesome-icon icon="fa-solid fa-check" /></li>
                          <li class="flag"><font-awesome-icon icon="fa-solid fa-check" /></li>
                          <li class="flag"><font-awesome-icon icon="fa-solid fa-check" /></li>
                          <li class="flag"><font-awesome-icon icon="fa-solid fa-check" /></li>
                          <li><font-awesome-icon icon="fa-solid fa-xmark" /></li>
                          <li><font-awesome-icon icon="fa-solid fa-xmark" /></li>
                      </ul>
                      <div class="button btn-blue"><button>GET IT NOW</button></div>
                  </div> 
                </div>

                <!-- 4 colonna -->
                <div class="col colomn title-col">
                   <div class="title-col">
                      <img src="img/h5-custom-icon-9.png" alt="">
                       <h3><strong>Advanced</strong></h3>
                      <p><strong>$88</strong></p>
                    </div>
                 
                  <div>
                      <ul>
                          <li>6</li>
                          <li>30 Days</li>
                          <li class="flag"><font-awesome-icon icon="fa-solid fa-check" /></li>
                          <li class="flag"><font-awesome-icon icon="fa-solid fa-check" /></li>
                          <li class="flag"><font-awesome-icon icon="fa-solid fa-check" /></li>
                          <li class="flag"><font-awesome-icon icon="fa-solid fa-check" /></li>
                          <li class="flag"><font-awesome-icon icon="fa-solid fa-check" /></li>
                          <li class="flag"><font-awesome-icon icon="fa-solid fa-check" /></li>
                      </ul>
                      <div class="button"><button>GET IT NOW</button></div>
                  </div> 
                </div>
      </div> 

      <!-- icone laterali -->

      <div class="circle">
        <font-awesome-icon icon="fa-solid fa-circle-notch" class="icon" />
      </div>

      <div class="cart">
        <font-awesome-icon class="icon" icon="fa-solid fa-cart-shopping" />
      </div>
      
      <div class="button-component">
          <ButtonComponent />
    </div>
    </div>
    
    <hr>
  </div>
</template>

<script>

import ButtonComponent from '@/components/ButtonComponent.vue'

// FONTAWESONE
  /* import the fontawesome core */
  import { library } from '@fortawesome/fontawesome-svg-core'

  /* import specific icons */
  import { faCheck } from '@fortawesome/free-solid-svg-icons'
  import { faXmark } from '@fortawesome/free-solid-svg-icons'
  import { faCartShopping } from '@fortawesome/free-solid-svg-icons'
  import { faCircleNotch } from '@fortawesome/free-solid-svg-icons'

  /* import font awesome icon component */
  import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome'

  /* add icons to the library */
  library.add(faCheck, faXmark, faCartShopping, faCircleNotch)

// FINE FONTAWESONE

export default {
    name: 'PrincingComponent',
    components: {
      FontAwesomeIcon,
      ButtonComponent
    }
}
</script>

<style scoped>

.title {
  padding-top: 20px;
  text-align: center;
}

.title h2 {
  font-size: 40px;
}

.title p {
  padding-top: 20px;
  color: grey;
}

.container {
  height: 800px;
  background-image: url('../../public/img/page-background-img.png');
  background-size: cover;
  margin: 100px auto;
  margin-bottom: 80px;
  width: 80%;
  position: relative;
}




/* colonne */

.col{
    width: 900px;
    border-bottom: 1px solid lightgrey;
}




/* LISTA */

ul {
  list-style-type: none;

}

li {
  padding: 15px;
  border: 1px solid grey;
}

.colomn {
  text-align: center;
}

.flag {
  color: #55acee;
}


.button {
  background-color: #f2f8fc;
  padding: 20px;
}

button {
  padding: 10px;
  border: 1px solid lightgrey;
  cursor: pointer;
}

.btn-blue button {
  background-color: #40c4ff;
  color: white;
}

.title-col {
  height: 150px;
  background-color: #f2f8fc;
}

.title-col-2 {
  background-color: #f2f8fc;
  height: 148px;
}

.title-col p {
  padding-top: 10px;
}

.title-col-first {
  height: 150px;
  padding-top: 60px;
}

.border-top-blue {
  border-top: 2px solid #40c4ff;
}

.col-container {
  margin-top: 50px;
  border: 1px solid lightgray;
  border-top: 2px solid #40c4ff;
  
}

.button-component {
  position: absolute;
  right: -40px;
  top: 320px;
}

hr {
  color: lightgray;
}



.cart {
  background-color: white;
  border: 0.5px solid lightgray;
  padding: 10px;
  position: absolute;
  right: -40px;
  top: 250px;
}

.cart .icon {
  color: #ef2853;
}

.circle .icon {
  color: white;

}

.circle {
  background-color: #ef2853;
  border: 0.5px solid lightgray;
  padding: 12px;
  position: absolute;
  right: -42px;
  top: 200px;
}

</style>