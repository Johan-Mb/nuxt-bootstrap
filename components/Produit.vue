<template>
    <div class="card" style="width: 18rem;">
        <div class="card-body">
            <h5 class="card-title">{{ nom }}</h5>
            <h6 class="card-subtitle mb-2 text-muted">Prix : {{ prix }}€</h6>
            <p class="card-text">Some quick example text to build on the card title and make up the bulk of the card's content.</p>
            <button v-if="role =='commander'" @click="$emit('commande', nom, prix)" class="btn btn-success">Ajouter au panier</button>
        </div>
    </div>
</template>

<script>
export default {
    name:"Produit",
    props: ['nom', "prix", "role"],
}
</script>
