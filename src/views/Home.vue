<template>
  <div class="home">
    <h1>Bienvenido   a Playapez</h1>
    <v-list>
      <v-subheader>Galeria</v-subheader>
      <v-list-item-group v-model="selectedItem" color="primary">
        <v-list-item v-for="(item, i) in items" :key="i">
          <v-list-item-icon>
            <v-img max-height="120" max-width="120" :src="item.image"></v-img>
          </v-list-item-icon>
          <v-list-item-content>
            <v-list-item-title v-text="item.name"></v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list-item-group>
    </v-list>
  </div>
</template>

<script>
export default {
  data() {
    return {
      selectedItem: 1,
      items: [
        { name: "Infraestructura", image: require("../assets/img/imagen1.png") },
        { name: "Tilapia Roja", image: require("../assets/img/imagen2.png") },
        { name: "Tanques Cultivo", image: require("../assets/img/imagen3.png") },
        { name: "Bandejas", image: require("../assets/img/imagen4.png") },
      ],
    };
  },
};
</script>
