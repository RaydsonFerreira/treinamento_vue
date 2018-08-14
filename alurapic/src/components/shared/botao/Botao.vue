<template>
    <button @click="disparaAcao()" class="botao botao-perigo">{{ rotulo }}</button>
</template>

<script>
export default {
    props: {
        tipo: {
            required: true,
            type: String
        },

        rotulo: {
            required: true,
            type: String
        }
    },

    methods:{
        disparaAcao(){
            if(confirm('Confirma Operação?'))
                this.$emit('botaoAtivado');
        }
    }
}
</script>

<style>
.botao {
    display: inline-block;
    padding: 10px;
    border-radius: 3px;
    margin: 10px;
    font-size: 1.2em;
}

.botao-perigo {background: firebrick;
    color: white;
}

.botao-padrao {
    background: darkcyan;
    color: white;
}
</style>
