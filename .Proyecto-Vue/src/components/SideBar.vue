<template>
    <div class="sidebar">
        <h2>Bienvenido</h2>
        <ul>
            <li>
                <router-link to="/contador">Contador</router-link>
            </li>
            <li>
                <router-link to="/lista-de-tareas">Lista de Tareas</router-link>
            </li>
            <li>
                <router-link to="/registrar">Registrar</router-link>
            </li>
            <li>
                <router-link to="/calcular">Calcular</router-link>
            </li>
        </ul>
    </div>
</template>

<script setup>

// import { ref, watch} from 'vue';


// const nombre = ref(registrarStore.nombre.value);
// const email = ref(registrarStore.email.value);

// watch(() => registrarStore.nombre, (newValue) => {
//     nombre.value = newValue;
// });

// watch(() => registrarStore.email, (newValue) => {
//     email.value = newValue;
// });

</script>

<style>
.sidebar{
    width: 150px;
    height: 150px;
    background-color: rgb(165, 167, 167);
    padding: 20px;
}
</style>