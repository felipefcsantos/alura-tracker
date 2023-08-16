<template>
    <button class="button" @click="clicado" :disabled="desabilitado">
        <span class="icon">
            <i :class="icone"></i>
        </span>
        <span>{{ nomeBotao }}</span>
    </button>
</template>

<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
    name: 'Botao',
    emits: ['clicado'],
    props: {
        nomeBotao: {
            type: String,
            required: true
        },
        icone: {
            type: String,
            required: true
        },
        desabilitado: {
            type: Boolean
        }
    },
    methods: {
        clicado() : void{
            this.$emit('clicado')
        }
    }
})
</script>

<style scoped></style>