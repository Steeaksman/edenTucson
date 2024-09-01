<template>
<!-- Set bckgrnd of header Div to black. Add a flexbox container. Use  justify-between
to set space between the two divs that hold the logo and links. Use items-center to
center links and logo on the y axis -->

<div class="bg-black flex justify-between items-center sticky">

  <!-- Left Side logo placed in a div  -->
<div class="text-white text-lg p-4 mx-6">
    <!-- StoneTigerDigital -->
     <NuxtLink to="/" class="text-white p-4">StoneTigerDigital</NuxtLink>
</div>


<div class="mx-6">
<!-- This is the right side navigation placed in a div -->

        <NuxtLink to="wednesday" class="text-white p-4">Wednesday</NuxtLink>
        <NuxtLink to="thursday" class="text-white p-4">Thursday</NuxtLink>
        <NuxtLink to="friday" class="text-white p-4">Friday</NuxtLink> 
        <NuxtLink to=  "saturday" class="text-white p-4">Saturday</NuxtLink> 
        <NuxtLink to=  "sunday" class="text-white p-4">Sunday</NuxtLink> 

</div>
</div>
<!-- end background div -->
</template>