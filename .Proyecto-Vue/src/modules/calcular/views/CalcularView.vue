<template>
<h3>Propiedades Comoutadas</h3>
<input type="text" name="" id="" v-model="valor">
{{ valorCalculado }}
<ResultadosSection :resultado="valorCalculado"></ResultadosSection>
</template>

<script setup>
import { ref , computed} from 'vue';
import ResultadosSection from '../components/ResultadosSection.vue';

const valor = ref('');
const valorCalculado = computed(()=>{
    return valor.value * 3
});
</script>

<style scoped>
</style>