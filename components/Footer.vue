<template>
    <div>
        <div class="bg-custom py-2 px-3">
         <b-row >
           <b-col md="12" class="px-5 py-1">
           <b-img left src="../assets/footer_logo.png" alt="footer" fluid class="bg-transparent" />
           </b-col>
         </b-row>
         <hr color="white"/>
         <b-row class="px-5 py-5">
            <b-col md="4" sm="12">
            <h6 class="text-title text-center pt-sm-3">No. 88 Sunset Bureau
            Sunset Road no. 88, Seminyak, Bali 80361</h6>
            <div class="container wrapper">
            <b-button class="px-5 py-3 btn-custom-header">Customer Service Number</b-button>
            
            <div class="py-1"></div>
            
            <b-button class="px-5 py-3 btn-custom-header">Company Email</b-button>
            </div>
            </b-col>
            
            <b-col md="4" sm="12">
            <div id='toolbar'>
            <div class='wrapper'>
            <h4 class="text-title text-center pt-sm-3">Guest Service</h4>
            
            <b-button-group vertical >
                <b-button class="py-2 btn-custom-header">Find A Property</b-button>
                <b-button class="py-2 btn-custom-header">Recommendations</b-button>
                <b-button class="py-2 btn-custom-header"><Nuxt-link to="./About" style="color:white;">About</Nuxt-link></b-button>
            </b-button-group>
            

            
            <b-button-group vertical>
                <b-button block class="py-3 px-5 btn-custom-header"><Nuxt-link to="./Teams" style="color:white;" >Team</Nuxt-link></b-button>
                <b-button block class="py-3 px-5 btn-custom-header">Career</b-button>
            </b-button-group>
            </div>
            </div>

            </b-col>
            
            <b-col md="4" >
            <div id='toolbar'>
            <div class='wrapper'>
            <h4 class="text-title text-center pt-sm-3">Owner Service</h4>
            <b-button-group vertical class="align-items-center">
                <b-button class="py-2 btn-custom-header">Become An Alterstay</b-button>
                <b-button class="py-2 btn-custom-header">Schedule Consultation</b-button>
                <b-button class="py-2 btn-custom-header">Owner Resources</b-button>
            </b-button-group>
            </div>
            </div>

            
         </b-col>
         </b-row>
         
         <hr color="white" />

         <b-row >
           <b-col md="12">
           <p class="text-center py-3">Copyright &copy; 2022, Alterstay. All Rights Reserved.</p>
           </b-col>
         </b-row>
        </div>
    </div>
</template>

<script>

</script> 

<style>

p{
    color:white;
    font-family: 'poppins';
}
.text-title{
    color: white;
}

.wrapper{
    text-align: center;
}
.bg-custom{
    background-color: #3D5C60;
}

.btn-custom-header{
    color: white;
    background-color: #3D5C60;
}

.padding-custom{
    margin-left: 25%;
}

#toolbar .wrapper {
    text-align: center;
}

@media (max-width:768px) {   
#toolbar .wrapper {
    margin-top: 10%;
}

}
</style>
