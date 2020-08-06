<template>
  <div id="mapid"></div>
</template>

<script>
import L from "leaflet";
import "leaflet/dist/leaflet.css";
export default {
  name: "leaflet-map",
  data() {
    return {
      map: null
    };
  },
  mounted: function() {
    this.map = L.map("mapid").setView([51.959, -8.623], 12);
    L.tileLayer("http://{s}.tile.osm.org/{z}/{x}/{y}.png", {
      attribution:
        '&copy; <a href="http://osm.org/copyright">OpenStreetMap</a> contributors'
    }).addTo(this.map);
  },
  beforeDestroy() {
    if (this.map) {
      this.map.remove();
    }
  }
};
</script>

<style>
#mapid {
  height: 100%;
  width: 100%;
}
</style>
