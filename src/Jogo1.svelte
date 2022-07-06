<svelte:head>
	<link rel="stylesheet" href="/styles/Jogostyle.css">
</svelte:head>

<script>
	//lógica do jogo(terá um arquivo svelte específico para ele)
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
let tabelaVazia = [ //tabela vazia e tabela resposta compõem as 3 cruzadas
	[],
	[],
	[],
	[],
	[],
	[],
	]

let tabelaResposta = [
	["A", "W", "Y", "Z", "K", "X","X","X","X","X"],  //testar com algo real, quadrados vazios e/com dicas, ou dicas fora do jogo 
	["B", "X", "X", "X", "X", "X","X","X","X","X"],
	["C", "X", "X", "X", "X", "X","X","X","X","X"],
	["X", "X", "X", "X", "X", "X","X","X","X","X"],
	["X", "X", "X", "X", "X", "X","X","X","X","X"],
	["X", "X", "X", "X", "X", "X","X","X","X","X"],
	] 


	//fazer um contador de acertos e erros definidos fora de um loop, e depois encaixalos para na função, os somatizar por erro e acerto
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
			{#each linha as dado,j}
				<td>
					<input type="text" maxlength="1" bind:value={tabelaVazia[i][j]}>
				</td>
			{/each} <!-- corrigir o erro na computação de tds no segundo loop each utilizando dado-->
		</tr>
	{/each}
</table>
	</center>
</section>



<!-- reaproveita o botão de voltar para o menu -->
