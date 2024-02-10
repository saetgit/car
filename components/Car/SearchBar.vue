<script setup>
const city=ref("")
// const router=useRouter();
const cityError=ref(false)
const handelSearch=()=>{
    // router.push(`/city/{city.value}/car`)

    if(!city.value){
        return cityError.value=true
    }
    navigateTo(`/city/{city.value}/car`)
}
</script>

<template>
    <!-- HOME SEARCH BAR -->
    <div
        class="font-serif text-2xl rounded-full bg-white flex justify-between overflow-hidden drop-shadow-2xl mx-auto">
        <input type="text" class="py-3 px-5 text-2xl rounded-full focus:outline-none"
            placeholder="Search by city..." v-model="city" :class="cityError?'border-red-500 border':''"/>
        <button class="bg-sky-500 px-10 text-white" @click="handelSearch()">Search</button>
    </div>
    <!-- HOME SEARCH BAR -->
</template>