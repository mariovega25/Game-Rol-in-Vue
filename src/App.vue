<template>
  <h1>En Construcción</h1>
  <div id="game">
  <playerstats :xp="state.xp" :health="state.health" :gold="state.gold"></playerstats>
  <controlsgame :buttons="buttons" @action="handleAction"></controlsgame>
  <monsterstats :name="monsterName" :health="state.health" :visible="showMonster"></monsterstats>  
  <gametext :text="state.text"></gametext>
  
  </div>
 
</template>

  <script setup>
  import playerstats from './components/playerstats/playerstats.vue';
  import controlsgame from './components/controlsgame/controlsgame.vue';
  import gametext from './components/gametext/gametext.vue';
  import monsterstats from './components/monsterstats/monsterstats.vue';  
  import {computed, reactive } from 'vue';

  const state = reactive({
    xp: 0,
    health:100,
    gold:50,
    currentWeaponIndex: 0,
    fighting: null,
    monsterHealth: 0,
    inventory:["stick"],
    currentLocationIndex: 0,
    text:"Welcome to Dragon Repeller...",
  });
  const showMonster = computed(()=> state.fighting !==null);
  const monsterName = computed(()=> state.fighting !== null? monsters[state.fighting].name:'');

 /*  const buttons = computed(()=> locations[state.currentLocationIndex]["button text"]);

  function handleAction(index){
    const actionFn = locations[state.currentLocationIndex]["button functions"][index];
    actionFn();
  } */

// Aqui Seguiria goStore(), goCave(), fightDragon(), attack(), etc., Adaptados a Vue

  </script>


<style scoped>
@import './assets/styles.css';

</style>
