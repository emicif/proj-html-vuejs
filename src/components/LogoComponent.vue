<template>
  <div class="container">
        <div class="button">
          <ButtonComponent />
        </div>
        <div class="flex loghi">
          <img alt="iAcademy-Logo" src="../../public/img/h5-client-5.png">
          <img alt="iAcademy-Logo" src="../../public/img/h5-client-1.png">
          <img alt="iAcademy-Logo" src="../../public/img/h5-client-2.png">
          <img alt="iAcademy-Logo" src="../../public/img/h5-client-1.png">
        </div>
      
  </div>
</template>

<script>

import ButtonComponent from '@/components/ButtonComponent.vue'


export default {
    name: 'LogoComponent',
    components: {
      ButtonComponent
    }
}
</script>

<style scoped>
.container {
  height: 200px;
}

.button {
  display: flex;
  justify-content: flex-end;
}

.loghi{
  justify-content: space-around;
}

</style>