<template>
 <main>
  <heroses/>
  <Form/>
  <Cards/>
  <Footer/>
 </main>
</template>

<script>
import Heroses from '@/components/heroses.vue'
import Cards from '@/components/cards.vue';
import Footer from '../components/footer.vue';
import Form from './form.vue';
 
// @ is an alias to /src

export default {
  name: 'HomeView',
  components: {
    Heroses,
    Cards,
    Footer,
    Form
}
}
</script>
