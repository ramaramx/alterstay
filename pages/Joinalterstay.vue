<template>
  <div>
    <b-img src="https://images.unsplash.com/photo-1608235375712-be654ace4420?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1074&q=80" fluid-grow alt="Responsive image" />
  
  <h3 class="text-center pt-5"> Why Join Us</h3>

  <b-card-group deck v-for="row in formattedClubs" class="py-5 container-fluid" align="center">
  <b-card v-for="club in row">
  <h3>{{club.title}}</h3>
  <p style="color:gray;">{{club.desc}}</p>
  </b-card>
  </b-card-group>
  </div>
</template>

<script>
export default {
  layout:'default',
    data: function () {
    return {
      clubs: [
          {id:1, title:'End To End Hospitality Ecosystem',  desc:'Our system covers sales and marketing, man management, purchasing, guest relation, revenue management, cost control, to finance and reporting.'},
          {id:2, title:'Economic of Scale',  desc:'Due to large portfolio, we are able to share resources between properties and have the leverage to bargain towards vendors and suppliers to get the best deal that cannot be achieved by managing single property.'},
          {id:3, title:'Profit Based Fee',  desc:'We are incentivized by making you profit, by not only bringing revenue and conversion, but also managing the expenses and maximizing efficiency.'}
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

</style>
