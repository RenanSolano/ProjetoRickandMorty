<script setup>
const personagem = defineProps(["name", "url", "gender", "species", "location", "episode"])
const personagemId = personagem.url.split('/')[5]
const imageUrl = "https://rickandmortyapi.com/api/character/avatar/" + personagemId + ".jpeg"
console.log(imageUrl)

</script>

<template>
  <div class="col-md-4">
    <div class="card p-2 mb-3" id="card">
      <img :src="imageUrl" height="280" alt="">
      <p class="text-center" id="listaText"><b>Nome: </b> {{personagem.name}}</p>
      <p class="text-center" id="listaText"><b>Especie: </b> {{personagem.species}}</p>
      <p class="text-center" id="listaText"><b>Genero: </b> {{personagem.gender}}</p>
      <p class="text-center" id="listaText"><b>Localidade: </b> {{personagem.location.name}}</p>
      <p class="text-center" id="listaText"><b>Quantidades de eps: </b> {{personagem.episode.length}}</p>
    </div>
  </div>
</template>

<style>
@import url('https://fonts.googleapis.com/css2?family=Bebas+Neue&family=Caveat:wght@400..700&family=DM+Serif+Display:ital@0;1&family=IBM+Plex+Serif:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;1,100;1,200;1,300;1,400;1,500;1,600;1,700&family=Jersey+15+Charted&family=Jersey+25&family=Noto+Sans+KR:wght@100..900&family=Playfair+Display:ital,wght@0,400..900;1,400..900&display=swap');

#listaText{
  color: #12b1c9ae;
  font-family: "IBM Plex Serif", serif;
  font-size: 20px;
}

#card{
  background-color: black;
}
</style>