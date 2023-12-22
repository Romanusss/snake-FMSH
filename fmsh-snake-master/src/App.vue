<template>
   <div class = "game">
      <header>
         <div>
            <h2 class = "Name">Змейка</h2>
            <h2 class = "Scoretext">Score: {{ score }}</h2>
         </div>
      </header>
   <GameBoard @score="onScore" />
   </div>
</template>

<script setup>
import GameBoard from './components/GameBoard.vue'
import { ref } from 'vue'

const score = ref(0)

function onScore()
{
   score.value++
}
</script>
<style>
body{
   background-color: rgb(6, 214, 34);
}
.Name {
   text-align: center
   
}

</style>