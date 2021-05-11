<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <DropDown></DropDown>
  </div>
</template>

<script>
// @ is an alias to /src
import DropDown from '@/components/DropDown.vue'

export default {
  name: 'Home',
  components: {
    DropDown
  }
}
</script>
