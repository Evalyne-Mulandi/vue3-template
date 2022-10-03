<template>
    <main>
      
      <Form @submit="onSubmit" :validation-schema="schema" class=" mt-3 flex flex-col gap-2  mx-auto justify-center items-center p-1 max-w-lg 
          bg-slate-100 text-black rounded-md">
          <div class="flex justify-center items-center font-extrabold font-mono">
        SignUp
      </div>
      <Field name="firstName" type="text" class=" rounded-md flex justify-center items-center gap-2 flex-col" placeholder="Enter your first name"/>
      <ErrorMessage name="firstName" class="text-red-600" />

      <Field name="lastName" type="text"  class=" rounded-md flex justify-center items-center gap-2 flex-col" placeholder="Enter your last name"/>
      <ErrorMessage name="lastName" class="text-red-600"/>

      <Field name="phoneNumber" type="number" class="rounded-md flex justify-center items-center gap-2 flex-col" placeholder="Enter your phone number" />
      <ErrorMessage name="phoneNumber" class="text-red-600" />

      <Field name="Email" type="email" class=" rounded-md flex justify-center items-center gap-2 flex-col" placeholder="Enter your email"/>
      <ErrorMessage name="Email"  class="text-red-600"/>

      <Field name="password" type="password"  class=" rounded-md flex justify-center items-center gap-2 flex-col" placeholder="Enter your password"/>
      <ErrorMessage name="password"  class="text-red-600"/>
      
      <button class=" rounded-lg px-4 py-2  gap-2 text-white bg-slate-500">Submit</button>
    </Form></main>
     
      
      </template>
  
    <script setup>   
    import { Form, Field, ErrorMessage } from 'vee-validate';
    import * as yup from 'yup';
     
       const schema = yup.object({
            Email: yup.string().required().email(),
            password: yup.string().required().min(8),
            phoneNumber: yup.number().required().min(10),
            lastName: yup.string().required(),
            firstName: yup.string().required()
          });
    function submit(values){
      console.log(values);  
    }
    
    
    </script>