<template>
    <div class="citacoes">
        <span>
            <button @click="numero--">&lt;</button>
            <button @click="numero++">&gt;</button>
        </span>
        <Citacao>
            <h3 slot="fonte">Fonte:</h3>
            <h3 slot="fonte">{{ citacoes[indice].fonte }}</h3>
            <p slot="texto">Citação:</p>
            <p slot="texto">{{ citacoes[indice].texto }}</p>
            <h6 slot="autor">Autor:</h6>
            <h6 slot="autor">{{ citacoes[indice].autor }}</h6>
        </Citacao>
    </div>
</template>

<script>
import Citacao from './Citacao.vue'
export default {
    components: { Citacao },
    data() {
        return {
            numero: 0,
            citacoes: [{
                fonte: 'Jornal do Empreendedor:',
                texto: 'Lembre-se sempre que você é absolutamente único. Assim como todos os outros.',
                autor: 'By: Margaret Mead'
            }, { 
                fonte: 'Frases de Mãe:',
                texto: 'Isso não é um quarto, é um chiqueiro.',
                autor: 'By: Roberta'
            }, {
                fonte: 'Frases de Pai:',
                texto: 'Vou contar até 3! ( 1 , 2 , 2.5... )',
                autor: 'By: Gustavo'
            }]
        }
    },
    computed: {
        indice() {
            return Math.abs(this.numero % 3)
        }
    }
}
</script>

<style scoped>
    .citacoes {
        display: flex;
        flex-direction: column;
        align-items: center;
    }
</style>
