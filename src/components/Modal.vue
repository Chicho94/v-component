<template>
  <div>
    <button @click="toggle">Modal</button>
    <teleport to='body'>

      <div v-show="show" class="modal">
        <h1>Este es el titulo</h1>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
        <button @click="toggle">x</button>
      </div>
    </teleport>
  </div>
</template>

<script>
export default {
  name: 'VmModal',
  props: {},
  data(){
    return{
      show:false,
    }
  },
  methods:{
    toggle(){
      this.show=!this.show;
    }
  }
}
</script>
