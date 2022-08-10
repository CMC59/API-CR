<template>
   <div class="container">

   <h1 class="my-4">App Clash Royale avec Vue.js</h1>

    <div class="form-groupe mb-5">
        <label for="idplayer">Entrez l'id d'un joueur</label>
        <input 
        id="idplayer" 
        type="text"
        class="form-control"
        v-model="requete"
        
        >

    </div>
    <div class="card text-center m-3">
        <div class="card-body">{{ retour }}</div>
    </div>
    <div class="w-75 m-auto">
        <h3 class="text-center mb-3">Info Joueur</h3>
        <div class="card text-center p-5">
            <p class="texte-affichage">
                Arène : 10{{ retour }}
            </p>
            <p class="texte-affichage">
                Niveau Tour du Roi : 11
            </p>
        </div>

    </div>



   </div>
</template>

<script>

import axios from 'axios'
//import { config } from 'vue/types/umd'

export default{
   name:'Cr',
   data() {
       return {
           retour: null,
           requete:'',
           info: undefined,       
              };
            }, 
    methods: {
         fetchData(){
            const token = "eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzUxMiIsImtpZCI6IjI4YTMxOGY3LTAwMDAtYTFlYi03ZmExLTJjNzQzM2M2Y2NhNSJ9.eyJpc3MiOiJzdXBlcmNlbGwiLCJhdWQiOiJzdXBlcmNlbGw6Z2FtZWFwaSIsImp0aSI6IjNmODJhZjg0LTYyZmItNGVhYy04YjRmLTc0N2U5ZTUwN2U4MSIsImlhdCI6MTY1NzIzMjc3Nywic3ViIjoiZGV2ZWxvcGVyLzM1MmE2ZTJmLTRiNWMtNTM2Ni02M2MyLWFmZmUwY2I3ZTcxYSIsInNjb3BlcyI6WyJyb3lhbGUiXSwibGltaXRzIjpbeyJ0aWVyIjoiZGV2ZWxvcGVyL3NpbHZlciIsInR5cGUiOiJ0aHJvdHRsaW5nIn0seyJjaWRycyI6WyI4OC4xNzIuMTQxLjE3MCJdLCJ0eXBlIjoiY2xpZW50In1dfQ.Oh1XFt6nah9m_o93fTq2vOMnpRi9E7cv4gmAPgy1fLvXlEjLl9Neo5TaoPAm8sL9g6TR7heojc4-WGbu9t96fg"
            const adresse = "https://api.clashroyale.com/v1/tournaments"  
            const headers = { Authorization: `Bearer ${this.token}` }
            request.defaults.headers.common['Authorization'] = `Bearer ${this.token}`;
            axios.get(`${adresse}`, { headers })
            .then(response => console.log(response)
        )}
            },     
            mounted() {
     // GET request using fetch with set headers
        this.fetchData()      
                      },
            }
 </script>

<style>
</style>