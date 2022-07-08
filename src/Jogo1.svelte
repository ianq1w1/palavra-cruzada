<svelte:head>
	<link rel="stylesheet" href="/styles/Jogostyle.css">
</svelte:head>

<script>

function Iguais(tab1,tab2){	
	for(let i=0; i < tab2.length; i++){
		for (let j=0; j < tab2[i].length; j++){
			if(tab1[i][j] == tab2[i][j]){
				return i
			}
		}	
	}
}

function Contagem(tabVazia,tabResposta) {
 let acertos = 0

	 if(Iguais(tabVazia,tabResposta)){
		return acertos ++
	}
	console.log(acertos)
}
	//estrutura do jogo
let tabelaVazia = [ 
	["A","B","",""],
	["","","",""],
	["","","",""]
	]
let tabelaResposta = [
	["A", "B", "C", "D"],  
	["E", "F", "G", "H"],
	["I", "J", "K", "L"]
	] 

Contagem(tabelaVazia,tabelaResposta)
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
					<input maxlength="1" bind:value={tabelaVazia[i][j]}>
				</td>
			{/each} <!-- corrigir o erro na computação de tds no segundo loop each utilizando dado-->
		</tr>
	{/each}
</table>
	</center>
</section>



<!-- reaproveita o botão de voltar para o menu -->



