<svelte:head>
	<link rel="stylesheet" href="/styles/Jogostyle.css">
</svelte:head>

<script>

function Contagem(tab1,tab2){	
let acertos = 0
	
	for(let L=0; L < tab1.length; L++){
		for (let C=0; C < tab1[L].length; C++){
			if(tab1[L][C] == tab2[L][C]){
				acertos++
			}
		}	
	}

console.log(acertos)
}

function Preencher(){
	let letras = document.getElementById('resposta')
	tabelaVazia.push(letras)
	console.log(tabelaVazia)
}




let tabelaVazia = [ 
	[],
	[],
	[]
	]

let tabelaResposta = [
	[22 ,"b", "c", "d"],  
	["e", "f", "g", "h"],
	["i", "j", "k", "l"]
	] 


</script>
<!--modelo do jogo em html-->
<h2>
	Cruzada nível 1
</h2>

<section>
	<center>	
<table>
	{#each tabelaResposta as linha,i}
		<tr>
			{#each linha as tabelaResposta,j}	
				<td>
						<input maxlength="1" bind:value={tabelaVazia[i][j]} id="resposta">
					</td>
			{/each} 
		</tr>
	{/each}
</table>
	<button on:click="{()=> Preencher()}" on:click="{()=> Contagem(tabelaVazia,tabelaResposta)}">ENVIAR ESSA BOMBA!</button>	
</center>
</section>



<!-- reaproveita o botão de voltar para o menu -->


