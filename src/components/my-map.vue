
<template>
<div class="container">
        <div class="jumbotron">
            <h4 class="display-4">
                My Location
            </h4>
            <p class="lead">Enter your latitude and longitude to display your location on a Google Map</p>
            <hr>
            <form id = "map">
                <div class="form-row">
                    <div class="col">
                        <input type="text" v-model="latInput"name="lat" id="lat" placeholder="Latitude" class="form-control">
                    </div>
                    <div class="col">
                        <input  type="text" v-model="lonInput" name="lon" id="lon" placeholder="Longitude" class="form-control">
                    </div>
                </div>
                <div class="form-row">
                    <div class="col">
                        <input v-on:click="findLocation"type="submit" value="Show My Location" class="btn btn-primary mt-4" >
                    </div>
                </div>
            </form>
            <img v-bind:src="url"/>  
        </div>
    </div>
</template>

<script>
export default {
    name: 'myMap',
        data () {
            return {
                latInput:"",
                lonInput:"",
                url: ""
                
           
               
            }
        },
        methods: {
            findLocation: function(e){
                
                this.url = "https://maps.googleapis.com/maps/api/staticmap?center="+ this.latInput +","+ this.lonInput +"&zoom=13&size=400x400&maptype=roadmap&markers=color:Red%7%7C"+ this.latInput +","+ this.lonInput +"&key=AIzaSyB0zhZrdrIkQRp1ViP9XjuwPqgTU6wY2sM";
                e.preventDefault();
                
            }
        }
}
</script>