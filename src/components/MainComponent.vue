<template>
  <div>
    <SmallCard />
    <HomeTutoring />
    <ChildrenComponent />
    <SliderComponent />
    <LearningComponent />
    <CoursesComponent />
    <PrincingComponent />
    <LogoComponent />

  </div>
</template>

<script>

import SmallCard from '@/components/SmallCard.vue'
import HomeTutoring from '@/components/HomeTutoring.vue'
import ChildrenComponent from '@/components/ChildrenComponent.vue'
import SliderComponent from '@/components/SliderComponent.vue'
import LearningComponent from '@/components/LearningComponent.vue'
import CoursesComponent from '@/components/CoursesComponent.vue'
import PrincingComponent from '@/components/PrincingComponent.vue'
import LogoComponent from '@/components/LogoComponent.vue'



export default {
  name: 'MainComponent',
  components: {
    HomeTutoring,
    SmallCard,
    ChildrenComponent,
    SliderComponent,
    LearningComponent,
    CoursesComponent,
    PrincingComponent,
    LogoComponent,
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
