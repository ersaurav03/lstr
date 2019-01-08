<template>
  <div class="home">
<Abc></Abc>
<JSMDJ></JSMDJ>
  </div>
</template>

<script>
// @ is an alias to /src
import Abc from './abc.vue';
import JSMDJ from './JSMDJ.vue'

export default {
  name: 'home',
  components: {
  Abc,
  JSMDJ
  // JSMPJ
  }
}
</script>
