<template>
  <footer>
    <Subscribe />
    <h3>IMAGES</h3>
    <Contacts />
    <div>
      <p>Copyright</p>
    </div>
  </footer>
</template>

<script>
import Subscribe from './Subscribe.vue'
import Contacts from './Contacts.vue'

export default {
  name: 'Footer',
  components:{
    Subscribe,
    Contacts
  }
}
</script>

<style lang="scss">

</style>