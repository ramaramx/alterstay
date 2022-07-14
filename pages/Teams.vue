<template>
    <div>
    <div class="container py-1">  
        <h3 class="text-center py-5" style="font-weight:300;">Alterstay is a digital hospitality ecosystem where we envision an always-improving experience for all hospitality stakeholder. We are dedicated for a different and better guest experience, owning experience, and team working experience, through continuous improvement and digitalization. 
        </h3>
        <h3 class="text-center pb-5">Alterstay: Experience Different</h3>
        <b-img src="https://images.unsplash.com/photo-1531545514256-b1400bc00f31?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1074&q=80" fluid alt=""></b-img>
            
            <h3 class="text-center mt-5">Core Value</h3>
            <b-card-group deck class="py-2 mb-5">
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

        <b-card-group deck v-for="row in formattedClubs" class="py-5">
        <b-card  v-for="club in row"
                img-src="https://images.unsplash.com/photo-1635003913011-95971abba560?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=756&q=80"
                img-alt="Img"
                img-top
                >
            <h4 class="card-title text-center">
                {{club.name}}
            </h4>
            <p class="card-text text-center" style="color:black;">
                {{club.job}}
            </p>

        </b-card>
    </b-card-group>
    </div>
   <hr />
    <div class="container wrapper pt-5 pb-5">
     
        <h3 class="text-center">We are always hiring! Join Us</h3>
        <b-button class="btn-custom-green"> Join With Us</b-button>
    
    </div>
    <hr />
    </div>

</template>

<script>

export default {
  layout:'default',
    data: function () {
    return {
      clubs: [
          {id:1, name:'Rama',  job:'Web Developer'},
          {id:2, name:'Rama',  job:'UI/UX'},
          {id:3, name:'Rama',  job:'UI/ux'},
          {id:4, name:'Rama',  job:'Web Developer'},
          {id:5, name:'Rama',  job:'Web Developer'},
          {id:6, name:'Rama',  job:'Web Developer'},
          {id:7, name:'Rama',  job:'Web Developer'},
          {id:8, name:'Rama',  job:'Web Developer'}
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
  },
  scrollToTop: true
}

</script>

<style>
 .wrapper {
    text-align: center;
}

.btn-custom-green{
    color: white;
    background-color: #3D5C60;
    text-align: center;
}

.btn-custom-green:hover{
    color: white;
    background-color: #293e41;
    transition: 0.5s;
}
</style>
