<template>
      <div class="flex flex-col items-center p-8">
       
      <h1> 
        This is the donnytest page 
        It calls donny.ts on the server using the useFetch composable   
        The  server returns a json datatype
    </h1>

<!-- DISPLAY THE  returned DATA FROM THE SERVER CALL -->
<!-- <ul>
  <li>
    <img :src="scizor.sprite"/>
  </li>
  <li>
    {{ scizor.id }}: {{ scizor.name }}
  </li>
  </ul> -->
{{ data }}
    
    
    <UButton color ="red" to="/vidtest5">Lingus by Snarky Puppy</UButton>
    <UButton color ="blue" to="/vidtest6">Bearologist</UButton>
</div>
  </template>


  <script setup>
  
  //CALL THE ENDPOINT ON THE SERVER with the UseFetch composable 
  const { data} = await useFetch(
    '/api/donny'
  )
</script>
  