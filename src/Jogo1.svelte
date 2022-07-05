<svelte:head>
	<link rel="stylesheet" href="/styles/Jogostyle.css">
</svelte:head>

<script>
	//lógica do jogo
function Contagem(tabVazia,tabResposta) {
	for(let i=0; i<=tabResposta.length; i++){
		for (let j=0; j<=tabResposta[i].length; j++){
			return tabResposta[i][j]
			return tabResposta[i][j] 
	}
}
	if(tabResposta[i][j] === tabVazia[i][j]){
			alert('boa')
	}else if(tabResposta[i][j] !== tabVazia[i][j]){
		alert('opa tá errado irmão')
}

}

	//estrutura do jogo
let tabelaVazia = [
	[],
	[],
	[],
	[],
	[],
	[],
	]

let tabelaResposta = [
	["A", "W", "Y", "Z", "K", "X","X","X","X","X"],
	["B", "X", "X", "X", "X", "X","X","X","X","X"],
	["C", "X", "X", "X", "X", "X","X","X","X","X"],
	["X", "X", "X", "X", "X", "X","X","X","X","X"],
	["X", "X", "X", "X", "X", "X","X","X","X","X"],
	["X", "X", "X", "X", "X", "X","X","X","X","X"],
	] 


	//fazer um contador de acertos e erros na função
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
			{#each tabelaResposta as dado,j}
				<td>
					<input type="text" maxlength="1" bind:value={tabelaVazia[i][j]}>
				</td>
			{/each}
		</tr>
	{/each}
</table>
	</center>
</section>



<!-- reaproveita o botão de voltar para o menu -->
