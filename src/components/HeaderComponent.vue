<template>
  <div >
    <div class="header-style">
      <img alt="iAcademy-Logo" src="../../public/img/logo-light.png">
      <nav></nav>
      <h1>Contemporary Ideas</h1>
      <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Adipisci dolore voluptate minima laboriosam ab iusto iste, officia nihil facere sint totam fugit officiis est.</p>
      <button>Register Now</button>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HeaderComponent',

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

.header-style{
  height: 600px;
  width: 100%;
  margin: 0px auto;
  background-image: url("../../public/img/course-9-f-img.jpg");
  background-repeat: no-repeat;
  color: white;
}

</style>
