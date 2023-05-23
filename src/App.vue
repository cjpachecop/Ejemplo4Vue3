<script setup>
import { ref, computed } from 'vue'
const users = [
{
  name: 'Jhon',
  lastname: 'Doe',
  age: '20'
},
{
  name: 'Jane',
  lastname: 'Doe',
  age: '30'
}

]

const msg = 'Happy'
const num = ref(0)

num.value = 2
const computado = computed(function (){
  return num.value > 0 ? num.value * 2 : 0
})

const mostrar = () => {
//alert('Me estan llamando')
console.log('Me estan llamando')

}
</script>

<template>
Hola Mundo {{ msg }}<br>
valor {{ num }}<br>
{{ mostrar()}}<br>
Valor computado {{ computado }}
<div v-for="(user, index) in users" :key="index">
 Nombre Completo {{ user.name }} {{  user.lastname}} <br>
 <span v-if="user.age">
  Edad: {{ user.age }}
 </span>
 
</div>
</template>

<style scoped>

</style>
