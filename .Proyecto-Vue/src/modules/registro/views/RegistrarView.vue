<template>
    <div>
        <h2>Formulario de Registro</h2>
        <Form :validation-schema="schema" @submit="onSubmit">
            <div class="form">
                <label for="nombre">Nombre : </label>
                <Field v-model="nombre" type="text" name="nombre" placeholder="ingrese su nombre" id="nombre"/>
                <ErrorMessage name="nombre"></ErrorMessage>
            </div>
            <div class="form">
                <label for="correo">Correo : </label>
                <Field v-model="email" type="text" name="email" placeholder="ingrese su email" id="email"/>
                <ErrorMessage name="email"></ErrorMessage>
            </div>
            <div class="form"> 
                <button type="submit"> Registrar </button>
            </div>
        </Form>

    </div>
</template>

<script setup>
import { Form,Field,ErrorMessage } from 'vee-validate';
import { schema } from '../schemas/validationSchema';
import { useRegistrarStore } from '../stores/registrarStore';
import { ref } from 'vue';

const registrarStore = useRegistrarStore();
const nombre = ref('');
const email = ref ('');
const onSubmit = () => {
    registrarStore.guardarRegistro(nombre.value, email.value);
    console.log('se ha enviado el formuliario');
}
</script>

<style scoped>
.form{
    margin-bottom: 10px;
}
</style>