<template>
  <div>
      <h2>The Trusted Name</h2>
      <h2>for In-Home Tutoring.</h2>
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

</style>