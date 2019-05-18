<template>
<div class="map container">
    <img v-bind:src="url">
</div>
</template>

<<script>
export default {
    name: 'map',
        data () {
            return {
                url : 'https://maps.googleapis.com/maps/api/staticmap?center=34.0522,-118.2437&zoom=13&size=1000x1000&maptype=roadmap&markers=color:Red%7%7C34.0522,-118.2437&key=AIzaSyB0zhZrdrIkQRp1ViP9XjuwPqgTU6wY2sM'
            }
        }
}
</script>