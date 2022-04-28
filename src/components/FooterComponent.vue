<template>
  <div>
    <footer >
      <div class="flex jcbeetwewn">

  <!-- footer-top -->    
          <!-- prima colonna -->
            <div class="first-column pl40">
              <img alt="iAcademy-Logo" src="../../public/img/footer-logo-1.png">
              <ul>
                <li>Proving Life Changing</li>
                <li>Experiences Through</li>
                <li>Education. Class That Fit Your</li>
                <li>Busy Life. Closer to Home</li>
              </ul>
              <!-- icona -->
                <div class="flex icon number">
                    <font-awesome-icon icon="fa-solid fa-phone"/>
                    <p>1-677-124-44227</p>
                </div>
                <div class="flex icon number">
                    <font-awesome-icon icon="fa-regular fa-clock"/>
                    <p>Mon - Sat 8.00 - 18.00</p>
                </div>
            </div>

            <!-- seconda colonna -->
            <div class="second-column pl40">
              <h3>Popular Courses</h3>
              <div class="sottotitle">
                <p><strong>Business English</strong></p>
                  <p>Preston Marshall</p>
              </div>

                <div class="sottotitle">
                <p><strong>Social Computing</strong></p>
                  <p>David Sanders</p>
              </div>

                <div class="sottotitle">
                  <p><strong>Learn Spanish</strong></p>
                  <p>Jennie King</p>
                </div>
            </div>

            <div class="third-column pl40">
              <h3>Support</h3>
              <p>User dashboard</p>
              <p>Contact Us</p>
              <p>FAQ</p>
              <p>Course Offer</p>
              <p>Events</p>
            </div>

            <div class="last-column pl60">
              <h3>Flexible Learning</h3>
              <img alt="iAcademy-Logo" src="../../public/img/footer-img-1.png">
            </div>
        </div>
 <!-- fine footer-top -->

        <hr>

 <!-- inizio footer-bottom -->
      <div class="footer-bottom flex">
        <p>Copyright 2017 <font-awesome-icon icon="fa-regular fa-copyright"/> Mikado Themes</p>
        <div class="flex column-right">
          <p>CALL +44 300 303 0266</p>
          <p>FOLLOW US</p>
          
        </div>
        
      </div>


    </footer>
  </div>
</template>

<script>

// FONTAWESONE
  /* import the fontawesome core */
  import { library } from '@fortawesome/fontawesome-svg-core'

  /* import specific icons */
  import { faPhone } from '@fortawesome/free-solid-svg-icons'
  import { faClock } from '@fortawesome/free-regular-svg-icons'
  import { faCopyright } from '@fortawesome/free-regular-svg-icons'
 
  /* import font awesome icon component */
  import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome'

  /* add icons to the library */
  library.add(faPhone, faClock, faCopyright)

// FINE FONTAWESONE



export default {
  name: 'FooterComponent',
  components: {
    FontAwesomeIcon
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">


//utilites
.jcbeetwewn {
  justify-content: space-between;
}

.pl40 {
  padding-left: 40px;
}

.pl60 {
  padding-left: 100px;
}

footer {
  background-color: black;
  height: 500px;
  justify-content: space-between;
  color: grey;
  padding-top: 100px;
  ul {
    list-style-type: none;
    li {
       padding-top: 10px;
    }
  }

  .first-column {
    .icon {
      padding-top: 30px;
    }
  }

  .last-column {
    padding-right: 20px;
  }

  .last-column{
   img{
     height: 100px;
   }
  }
}

.sottotitle{
  padding-top: 20px ;
}

hr {
  margin-top: 50px;
  
}

.footer-bottom{
  padding-top: 50px;
  padding-left: 20px;
  padding-right: 20px;
  justify-content: space-between;
}

.number p{
  padding-left: 10px;

}

.third-column h3 {
  padding-bottom: 10px;
}

.third-column p {
  padding-top: 10px;
}

.column-right p {
  padding-right: 10px;
}

</style>
