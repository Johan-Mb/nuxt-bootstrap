<template>
  <h1 class="display-1">Accueil</h1>
  <!-- <Produit v-for="produit in produits" 
      v-bind:nom="produit.nom" 
      v-bind:prix="produit.prix" 
      v-bind:key="produit.id" 
  /> -->
</template>

<script>
import Produit from '@/components/Produit.vue'
export default {
  components: {
        Produit
    },
  name: ''
}
</script>
