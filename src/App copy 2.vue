<template>
    
    <div class="background" :style="backgroundStyle">

      <div class="button-container">
        <div class="float-button create-button">
          <i class="fa-solid fa-plus"></i>
          Create room 
        </div>
        <br>
        

        <div class="float-button join-button">
          <i class="fa-solid fa-door-open"></i>
          Join room 
        </div>
        <br>

        <div class="float-button join-button">
          <i class="fa-solid fa-magnifying-glass"></i>
          Check room 
        </div>
        <br>

      </div>

      <!-- <div class="button-container">
        
          <div class="child">
            <i class="fa-solid fa-plus"></i>
            <br>
            Create room 
          </div>

          <div class="child">
            <i class="fa-solid fa-door-open"></i>
            <br>
            Join room
          </div>

          <div class="child">
            <i class="fa-solid fa-magnifying-glass"></i>
            <br>
            Check room 
          </div>

      </div> -->
    </div>
</template>

<script>
export default {
  data() {
    return {
      showLeft: true,

    };
  },
  computed: {
    backgroundStyle() {
      return {
        // backgroundImage: 'url(public/assets/background.png)', // Replace with your image path
        
        backgroundPosition: this.showLeft ? 'left center' : 'right center',
        backgroundRepeat: 'no-repeat',
        height: '100vh',
        transition: 'all 1s ease', // Smooth transition for sliding effect
      };
    },
  },
  methods: {
    slideBackground() {
      this.showLeft = !this.showLeft; 
    },
  },
};
</script>  
<style>
@import url('https://fonts.googleapis.com/css2?family=Pacifico&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Playfair+Display&display=swap');
body{
  margin: 0;
}
.background {
  /* background-image: url('../public/assets/images/background.png'); */
  background-image: linear-gradient(rgba(0, 0, 0, 0.3), rgba(0, 0, 0, 0.3)), url('../public/assets/images/background.png');
  width: 100%;
  position: relative;
  background-size: 150% 100%;
 
  max-width: 450px;
  max-height: 900px;
  margin: autoç;
}

.button-container{
  position: absolute;
  top: 15%;
  left: 50%;
  transform: translateX(-50%);
  border-radius: 10px;

  width: 80%;

  padding: 0px 20px;

  text-align: center;
}

.button-container .child{
  text-align: center;
}

.button-container .child i{
  background: darkgreen;
  color: white;
  widows: 120%;
  /* display: block; */
  border-radius: 50%;
  padding: 20px;
  margin-bottom: 10px;
  
  font-size: 2em;

}

.float-button{
  padding: 20px 60px;
  border-radius: 50vw;
  text-align: center;
  box-shadow: 4px 4px 8px rgba(0, 0, 0, 0.5);

  margin: auto;

  margin-bottom: 20px;

  display: inline-block;

  font-size: 1.25em;
  
}

.create-button{
  
  background: #F4EBD0;
  
}

.join-button{
  
  background: #F4EBD0;
  
}

.float-button i{
  margin-right: 10px;
}


</style>
