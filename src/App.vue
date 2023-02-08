<script setup>
import { RouterLink, RouterView } from "vue-router";
import Livre from "./components/Livre.vue";
</script>

<template>
  <header>
    <nav>
      <!--mettre les puces -->

      <ul id="menutop">
        <!-- RouterLink : des liens qui pointent vers le composant à afficher -->
        <!-- Voir la configuration des liens dans router/index.js -->
        <RouterLink to="/">Afficher les livres</RouterLink>
        <RouterLink to="/achats">Ajouter un livre</RouterLink>
        <RouterLink to="/achats">Supprimer un livre</RouterLink>
        <RouterLink to="/search">Modifier le stock</RouterLink>
        <RouterLink to="/stock">Rechercher un livre</RouterLink>
      </ul>
    </nav>
  </header>
  <p>
    <!--ajout de la photo -->
    <img alt="Vue logo" class="logo" src="@/assets/logo.png" />
  </p>

  <div id="test">
    <!-- Affichage des composants -->
    <Livre />
  </div>
</template>


<style scoped>
#menutop {
  background-color: #7d4d00;
  margin: 10px 0 0;
  padding: 0;
  height: 45px;
  display: flex;
}

li {
  flex: 1;
  list-style-type: none;
  line-height: 45px;
  text-align: center;
  border-color: white;
  border-style: solid;
  border-left: 1px;
}

RouterLink {
  flex: 1;
  list-style-type: none;
  line-height: 45px;
  text-align: center;
  border-color: white;
  border-style: solid;
  border-left: 1px;
  text-transform: uppercase;
  font-weight: bolder;
  font-size: 11px;
  color: white;
  text-decoration: none;
}
RouterLink:hover {
  color: black;
}

p img {
  float: left;
  max-width: 40%;
}
#test {
  float: right;
}
</style>
