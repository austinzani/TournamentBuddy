<template>

  <v-container id="hello">
    <v-row class = "text-center">
      <v-col>
        <h1 class="display-3 font-weight-bold mb-3">Welcome to Tourney Buddy!</h1>
      </v-col>
    </v-row>
    <v-row>
      <v-col col="12" sm="6">
        <v-img
          :src="require('../assets/brackets.jpg')"
          class="my-3"
          contain
        />
        <p>Come and see our many tournaments featuring all kinds of different sports and games. From magic to basketball, here at Tournament Buddy, we've got them all!</p>
        <v-btn @click="$router.push('/browse-tournaments')" class="d-flex">
           Browse Tournaments
        </v-btn>
      </v-col>
      <v-col cols="12" sm="6">
        <v-img
          :src="require('../assets/athletes.jpg')"
          class="my-3"
          contain
        />
        <p>We've got some fierce competitors in our selection of awesome teams! Register with us to become the best of the best!</p>
        <v-btn @click="$router.push('/register')" class="d-flex"> 
           Register
        </v-btn>
      </v-col>
    </v-row>
    <video id="video" playsinline autoplay muted loop poster=''>
        <source :src='require("@/assets/background.mp4")' type='video/mp4'></video>
  </v-container>
  

</template>

<script>
</script>


<style scoped >


#video{
  position: absolute;
  right: 0;
  bottom: 0;
  min-width: 100%;
  min-height: 100%;
  z-index: 0;
  filter: brightness(30%)

}
#hello>div{
  z-index: 1;
  position: relative;
}


</style>
