<script setup>
import { onMounted, reactive, ref } from 'vue';
import ListPersonagens from '../components/ListPersonagens.vue';

let personagens = reactive(ref());

onMounted(() => {
  fetch("https://rickandmortyapi.com/api/character")
  .then(response => response.json())
  .then(response => {
    personagens.value = response.results
    console.log(personagens)
  })
})

</script>

<template>
  <main>
    <div class="container">
      <div class="row mt-4">
        <div class="col-sm-12 col-md-12">
          <div class="card border-0">
            <div class="card-body row">
            <ListPersonagens 
            v-for="personagem in personagens" 
            :key="personagem.name" 
            :name="personagem.name"
            :url="personagem.url"
            :gender="personagem.gender"
            :species="personagem.species"
            :location="personagem.location"
            :episode="personagem.episode"
            />
            </div>
          </div>
        </div>
      </div>
    </div>
  </main>
</template>

<style>
.container{
  padding-top: 100px;
}
#textFooter{
  color:#12B0C9;
  font-weight: bold;
}
</style>
