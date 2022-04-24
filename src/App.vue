<template>
@TODO HERE
<div class="bg-current full">
<Header />
  <div class="container">
    <router-view/>
  </div>
</div>
  
</template>

<script>
import Header from '@/components/Header'

export default {
  components: {
    Header,

},
}
</script>