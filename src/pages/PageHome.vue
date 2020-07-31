<template>
  <div class="col-full">
    <h1>Welcome to the Forum</h1>
    <ForumList :forums="forums"/>
  </div>
</template>

<script>
import sourceData from '@/data'
import ForumList from '@/components/ForumList'
console.log(sourceData)

export default {
  components: {ForumList},

  data () {
    return {
      forums: Object.values(sourceData.forums),
      posts: sourceData.posts,
      users: sourceData.users
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

