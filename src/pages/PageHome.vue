<template>
  <div class="col-full push-top">
    <h1>Welcome to the Forum</h1>
    <CategoryList :categories="categories"/>
  </div>
</template>

<script>
import CategoryList from '@/components/CategoryList'

export default {
  components: {CategoryList},

  computed: {
    categories () {
      return Object.values(this.$store.state.categories)
    }
  }
}
</script>











/**  Giải thích về Object.value 
const kids =  {
  'one' : 'Mike',
  'two' : 'Will',
  'three' : 'Dustin',
  'four' : 'Lucas',
  'eleven' : 'Eleven'
}

kidNames = Object.values(kids); // return Mike, Will, Dustin, Lucas, Eleven 
kidKeys = Object.keys(kids); // return One, Two... Elenven

 */

