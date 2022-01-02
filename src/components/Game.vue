<template>
  <div>
    <h1>Game</h1>
    <h2>Select Norway</h2>
    <div class="map">
      <MapEurope class="map--image" @click="handle" />
    </div>
    <pre>{{ selected }}</pre>
  </div>
</template>

<script>
import MapEurope from "@/components/MapEurope.vue";
export default {
  components: {
    MapEurope,
  },
  data() {
    return {
      selected: null,
    };
  },
  methods: {
    handle(e) {
      this.selected = e.target.id;
    },
  },
};
</script>

<style lang="scss" scoped>
.map {
  max-width: 900px;
  .map--image {
    width: 100%;
  }
}
</style>
