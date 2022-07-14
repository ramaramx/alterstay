<template>

  <div>
  <b-carousel
    id="carousel-fade"
    style="text-shadow: 0px 0px 2px #000"
    fade
    indicators
    img-width="1024"
    img-height="200"
  >
    <b-carousel-slide
      alt="1"
      img-src="https://images.unsplash.com/photo-1608235375712-be654ace4420?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1074&q=80"
    >
    <b-button class="btn-custom-green">Check Property Now</b-button>
    </b-carousel-slide>
    <b-carousel-slide
      alt="2"
      img-src="https://images.unsplash.com/photo-1608235375712-be654ace4420?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1074&q=80"
    >
    <b-button class="btn-custom-green">Check Property Now</b-button>
    </b-carousel-slide>
    <b-carousel-slide
      alt="3"
      img-src="https://images.unsplash.com/photo-1608235375712-be654ace4420?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1074&q=80"
    >
   <b-button class="btn-custom-green">Check Property Now</b-button>
    </b-carousel-slide>
  </b-carousel>

  <div class="container py-5">
  <h3 class="text-center py-5" style="font-weight:300;">Alterstay is a digital hospitality ecosystem where we envision an always-improving experience for all hospitality stakeholder. We are dedicated for a different and better guest experience, owning experience, and team working experience, through continuous improvement and digitalization. 
  </h3>
  <h3 class="text-center">Alterstay: Experience Different</h3>
  
    <b-card-group deck class="py-5">
    <b-card align="center">
        <b-card-text style="color:black;">Standarized Services and Facilities</b-card-text>
      </b-card>
      <b-card align="center">
        <b-card-text style="color:black;">Fast Response Support and Help</b-card-text>
      </b-card>
      <b-card align="center">
        <b-card-text style="color:black;">Affordable Luxury</b-card-text>
      </b-card>
        <b-card align="center">
        <b-card-text style="color:black;">Seamless and Integrated Guest Experience</b-card-text>
      </b-card>
    </b-card-group>
  </div>

  <div class="container py-1">
  
  <b-row >
    <b-col md="10">
      <h3 class="text-left">Join Our Ecosystem</h3>
      <h3 class="text-left" style="font-weight:300; font-size: 16px;">Enjoy the most seamless and integrated guest experience through our vast ecosystem. 
      </h3>
    </b-col>

    <b-col md="2">
      <b-button class="btn-custom-green">Learn More</b-button>
    </b-col>
  </b-row>
  
  
  <!-- should be carousel slide card -->
    <b-card-group deck v-for="row in formattedClubs" class="py-5">
        <b-card  v-for="club in row"
                img-src="https://images.unsplash.com/photo-1570295999919-56ceb5ecca61?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=880&q=80"
                img-alt="Img"
                img-top>
            <h4 class="card-title text-center">
                {{club.description}}
            </h4>
            <p class="card-text text-center" style="color:black;">
                {{club.country}}
            </p>

        </b-card>
    </b-card-group>
   

    <b-row class="py-5">
    <b-col md="10">
      <h3 class="text-left">Own a property?</h3>
      <h3 class="text-left" style="font-weight:300; font-size: 16px;">Monetize your property and maximize its profits with us. 
      </h3>
    </b-col>

    <b-col md="2">
      <b-button class="btn-custom-green">Learn More</b-button>
    </b-col>
  </b-row>

  </div>
</div>

</template>

<script>

export default {
  layout:'default',
    data: function () {
    return {
      clubs: [
          {id:1, description:'The Kamare',  country:'Good Place'},
          {id:2, description:'Belle Astana',  country:'Nice Place'},
          {id:3, description:'Asayana Suites',  country:'Safe Place'}
      ]
    }
  },
   computed: {
      formattedClubs() {
          return this.clubs.reduce((c, n, i) => {
              if (i % 4 === 0) c.push([]);
              c[c.length - 1].push(n);
              return c;
          }, []);
      }
  }
};
</script>

<style>

h3{
    font-family: 'poppins';
    color: rgb(0, 0, 0);
}

.btn-custom-green{
    color: white;
    background-color: #3D5C60;
}

.btn-custom-green:hover{
    color: white;
    background-color: #293e41;
    transition: 0.5s;
}
</style>
