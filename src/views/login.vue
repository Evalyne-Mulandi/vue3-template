<template>
  <main class=" m-3  max-w-lg justify-center items-center  mx-auto rounded-lg">
    <Form  @submit="onSubmit" :validation-schema="schema"  class=" rounded-lg  flex-col gap-y-2 bg-slate-200 flex justify-center items-center  py-4 max-auto">
        <label  class=" m-3 uppercase font-mono font-extrabold">login</label>
        <Field name="Email" type="email" class=" rounded-md flex justify-center items-center gap-2 flex-col" placeholder="Enter your email"/>
      <ErrorMessage name="Email"  class="text-red-600"/>

      <Field name="password" type="password"  class=" rounded-md flex justify-center items-center gap-2 flex-col" placeholder="Enter your password"/>
      <ErrorMessage name="password"  class="text-red-600"/>
      
       <div class="">
        <input type="checkbox" class=" bg-indigo-700   m-2"><span>Remember me</span>
       </div>
       <div class=""> Don't have an account?<span><router-link to="/signup" class=" underline text-indigo-900">Signup</router-link></span></div>


    </Form>
  </main>


</template>
<script setup>   
  import { Form, Field, ErrorMessage } from 'vee-validate';
  import * as yup from 'yup';
   
     const schema = yup.object({
          Email: yup.string().required().email(),
          password: yup.string().required().min(8),
       
        });
  function submit(values){
    console.log(values);  
  }
</script>
<style>

</style>
