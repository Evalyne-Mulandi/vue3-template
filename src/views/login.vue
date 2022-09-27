<template>
    <form @submit.prevent="handleSubmit" class=" mt-3 flex flex-col  mx-auto justify-center items-center p-1 max-w-lg 
        bg-slate-100 text-black rounded-md">
<!--         <img src="@/assets/user.png" alt="" class=" rounded-full  mb-1"> -->
        <div class=" flex-col flex">
            <label> First name</label>
        
            <input v-model="firstName" type="text" class=" px-6     m-2 py-2 rounded-md mx-auto p-2" required placeholder="Enter your first name">
        </div>
        <div class="flex-col flex">
            <label> Last name</label>
            <input  v-model="lastName" type="text" class=" px-6  m-2 py-2 rounded-md mx-auto p-2"  required placeholder="Enter your Last name">
        </div>
    
        <div class="flex-col flex">
            <label> Phone number</label>
            <input v-model=" phoneNumber" type="text" class=" px-6  m-2 py-2 rounded-md mx-auto p-2 " required placeholder="Enter your Last name">
        </div>
        <div class="flex-col flex">
    
            <label> Email address</label>
            <input v-model=" emailAddress" type="text" class=" px-6  m-2 py-2 rounded-md mx-auto p-2  " required placeholder="Enter your Last name">
        </div>
        <div class="flex-col flex">
            <label> Password</label>
            <input  v-model=" password" type="text" class=" px-6  m-2 py-2 rounded-md mx-auto p-2"  required placeholder="Enter your Last name">
        </div>
        <div class="">
    
            <input type="submit" class=" rounded-md mx-auto px-6 py-2 hover:bg-indigo-500 bg-slate-900 text-white">
        </div>
    </form>
    <div v-show="data" class="flex justify-center items-center bg-orange-400 
     text-black mx-auto max-w-lg"> 
        <fieldset>
            
            <legend>Output</legend>
            {{firstName}}
            {{lastName}}
            {{phoneNumber}}
            {{emailAddress}}
            {{password}}
        </fieldset>
    </div>
    </template>
    
    <script>
    export default {
    data(){
        return{
            data:false,
            firstName:'',
            lastName:'',
            phoneNumber:'',
            emailAddress:'',
            password:'',
    
        }
    },
    methods:{
        handleSubmit(){
            this.data=true
        }
    }
    }
    </script>
    
    <style>
    
    </style>
    