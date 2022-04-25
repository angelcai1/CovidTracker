<template>
<div class="bg-red-50 h-screen">
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