<template>
 <main>
  <heroses/>
  <Cards/>
  <Footer/>
 </main>
</template>

<script>
import Heroses from '@/components/heroses.vue'
import Cards from '@/components/cards.vue';
import Footer from '../components/footer.vue';
 
// @ is an alias to /src

export default {
  name: 'HomeView',
  components: {
    Heroses,
    Cards,
    
    Footer,
}
}
</script>
