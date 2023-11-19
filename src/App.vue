<template>
    
    <div class="background" :style="backgroundStyle">
      <div class="button-container">
        
        <button @click="slideBackground"  :style="{ 'background-color': showLeft ? '#207269' : '#D76E6E'}">
          <span v-if="showLeft" >Join the party</span>
          <span v-else >welcome to party!</span>
        </button>
      </div>
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
  top: 50%;
  left: 50%;
  transform: translate(-50%,-50%);
}

.button-container button{
  padding: 10px 30px;
  /* background: #207269; */
  border-radius: 50vw;
  font-family: 'Playfair Display', serif;
    font-size: 18px; /* Adjust the font size as needed */
    color: #ffffff; /* Set the text color */

    box-shadow: 2px 2px 4px rgba(0, 0, 0, 0.2); 
    border: 0;

    transition: all .5s ease-in-out;



}


</style>
