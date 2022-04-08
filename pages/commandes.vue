<template>
    <div>
        <h1 class="display-1">Boutique</h1>
            <h2>Produits disponibles</h2>
            <div class="card-deck">
                <Produit v-for="produit in produits"
                    v-bind:nom="produit.nom"
                    role="commander"
                    v-bind:prix="produit.prix"
                    v-bind:key="produit.id"
                    v-on:commande="ajouterPanier"
                />
            </div>

            <h2>Commandes en cours</h2>
            <div class="card-deck">
                <Produit v-for="produit in commandes"
                    v-bind:nom="produit.nom"
                    v-bind:prix="produit.prix"
                    v-bind:key="produit.id"
                    role="affichage"
                />
            </div>
    </div>
</template>

<script>
import Produit from '@/components/Produit.vue'
export default {
    components: {
        Produit,
    },
  data(){
    return {
        produits: [
            {
                id: 1,
                nom: 'Produit 1',
                prix: 10
            },
            {
                id: 2,
                nom: 'Produit 2',
                prix: 20
            },
            {
                id: 3,
                nom: 'Produit 3',
                prix: 30
            }
        ],
        commandes: [
            {
                id: 1,
                nom: 'Produit 1',
                prix: 10
            }
        ]
    }
  },
  methods: {
    ajouterPanier(nom, prix){
        this.commandes.push({
            nom: nom,
            prix: prix
        })
    }
  }
}
</script>

<style scoped>
</style>
