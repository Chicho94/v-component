<template>
  <div>
    <div>{{ obj.count }}</div>
    <div>{{ aux }}</div>
  </div>
</template>

<script>
import { ref, reactive, watch } from "vue";

export default {
  name: 'vmHome',
  props: {},
  setup() {

    const aux = ref(0);
    const obj = reactive({ count: 0 });

    watch(() => obj, (valor, anterior) => {
      console.log(valor, anterior);
    });

    watch(aux, (valor, anterior) => {
      console.log(valor, anterior);
    });

    setInterval(() => { aux.value++; obj.count++ }, 5000);
    return { obj, aux }
  },
}
</script>
