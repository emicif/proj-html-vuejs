<template>
  <div>
        <div @click="scrollTop()" >
            <button><strong><font-awesome-icon icon="fas fa-angle-up" class="icon"/>TOP</strong></button>
        </div>

  </div>
</template>

<script>

// FONTAWESONE
  /* import the fontawesome core */
  import { library } from '@fortawesome/fontawesome-svg-core'

  /* import specific icons */
  import { faAngleUp } from '@fortawesome/free-solid-svg-icons'
  
  /* import font awesome icon component */
  import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome'

  /* add icons to the library */
  library.add(faAngleUp)
// FINE FONTAWESONE

export default {
    name: 'ButtonComponent',
    components: {
      FontAwesomeIcon
    },
    methods: {
      scrollTop(){
        window.scrollTo(0, top);
    }
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
  /* align-items: center; */
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
  cursor: pointer;
  
}

</style>