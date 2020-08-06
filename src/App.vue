<template>
  <div id="app">
    <div id="map-container">
      <leaflet-map></leaflet-map>
    </div>
  </div>
</template>

<script>
import LeafletMap from "./components/leaflet-map/LeafletMap.vue";
export default {
  name: "App",
  components: {
    "leaflet-map": LeafletMap
  }
};
</script>

<style>
#map-container {
  width: 100%;
  height: 50vh;
}
</style>
