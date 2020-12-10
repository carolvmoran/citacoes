<template>
	<div id="app">
		<Citacoes />
		<Sobre />
	</div>
</template>

<script>
import Citacoes from './components/Citacoes'
import Sobre from './components/Sobre'

export default {
	components: { Citacoes, Sobre }
}
</script>

<style>
	#app {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		height: 100vh;
		font-size: 1.6rem;
	}

	button {
        outline: none;
        padding: 5px 15px 10px;
        margin: 10px 5px;
        border-radius: 3px;
        font-size: 2rem;
        font-weight: 300;
		background-color: rgb(255, 208, 223);
        box-shadow:10px 10px 20px #ff5858;
        color:#ff5858 ;
        text-shadow: 1px 1px 2px black;
        border: 10px inset #ff5858;
        border-radius: 8px;
    }
</style>