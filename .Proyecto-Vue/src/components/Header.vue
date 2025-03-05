<template>
    <div class="header">
        <h3>Nombre: {{ registrarStore.nombre }}</h3>
        <h3>Email: {{registrarStore.email }}</h3>
        {{ mensajeRecibido }}<Weather></Weather>  
    </div>
</template>

<script setup>
import Weather from './Weather.vue';
import { useRegistrarStore } from '@/modules/registro/stores/registrarStore';
import { defineProps, ref,watch } from 'vue';
const props = defineProps(['mensaje']);
const mensajeRecibido = ref(props.mensaje);
watch(()=> props.mensaje,(newValue) =>{
    mensajeRecibido.value = newValue;
})
const registrarStore = useRegistrarStore();
</script>

<style scoped>
.header{
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 10px 20px;
    top: 0;
    right: 0;
    left: 0;
    background-color: rgb(165, 167, 167);
}

h3{
    margin: 0%;
}

</style>