<template>
   <main class=" md:flex hidden justify-around items-center mx-auto flex-row bg-teal-500">
    <div class=" uppercase text-black text-xl flex ">Coder</div>
    <nav class="flex justify-end items end   text-white pr-36 gap-x-2 p-3">
    <router-link to="/">Home</router-link> |
    <router-link to="/about">About</router-link> |
    <router-link to="/blog">Blog</router-link> |
    <router-link to="/contactus">Contact us</router-link> 
    
  </nav>
  <div class=" uppercase text-white font-mono font-extrabold flex justify-center items-center flex-row gap-x-1"><span><svg class="w-6 h-6 dark:text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 11l3-3m0 0l3 3m-3-3v8m0-13a9 9 0 110 18 9 9 0 010-18z"></path></svg></span><router-link to="/login">Signup</router-link></div>
  
   </main>
</template>

<script>
export default {

}
</script>

<style>

</style>