<template>
  <div class="container-top">

      <div class="title">
        <h2>The Trusted Name for In-Home Tutoring.</h2>
      </div>
      
      <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Similique fugiat dignissimos ipsam dolorem veritatis beatae aut alias ratione eum natus sed magni temporibus saepe, obcaecati incidunt tempora fuga! Accusamus, dignissimos!</p>
      <a href="#"><strong>LEARN MORE</strong></a>

      <div class="flex container">
        <img src="../../public/img/h5-img-1.jpg" alt="">
        <div>
            <ButtonComponent />
        </div>
      </div>
     
      
  </div>
</template>

<script>



import ButtonComponent from '@/components/ButtonComponent.vue'


export default {
    name: 'HomeTutoring',
    components: {
      ButtonComponent
    }
}
</script>

<style scoped>

.container-top {
  padding: 50px 50px;
}

.container-top p {
  padding: 20px 0px;
  color: grey;
}

a {
  text-decoration: none;
  color: #40C4FF;
}



/* button style */
.flex-column {
  display: flex;
  flex-direction: column; 
  align-items: center;
}

.container {
  align-items: center;
}

button {
  height: 50px;
  padding: 10px;
  background-color: #55acee;
  color: white;
  border: none;

}

.title {
  width: 250px;
}

</style>