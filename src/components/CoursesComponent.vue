<template>
  <div class="container">
        <div class="flex button">
          <ButtonComponent />
        </div>
      
        <h2>Popular Online Courses</h2>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Sapiente provident illo alias unde distinctio suscipit dolore? Saepe, eum. Quae sapiente minus suscipit quasi consectetur eius fugit delectus sunt dolorum nisi!</p>
        <CardComponent />
     
  </div>
</template>

<script>

import CardComponent from '@/components/CardComponent.vue'
import ButtonComponent from '@/components/ButtonComponent.vue'


export default {
    name: 'CoursesComponent',
    components: {
      CardComponent,
      ButtonComponent
    }
}
</script>

<style scoped>
.container {
  border-top: 1px solid grey;
  border-bottom: 1px solid grey;
  background-image: url('../../public/img/page-background-img.png');
  background-size: cover;
  text-align: center;
  padding-top: 30px;
  height: 1000px;
}


.button {
  justify-content: flex-end;
  padding-bottom: 40px;
}

h2 {
  font-size: 2.5rem;
  padding-bottom: 20px;
}

p {
  color: grey;
}

</style>