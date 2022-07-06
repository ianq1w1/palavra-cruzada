<svelte:head>
	<link rel="stylesheet" href="/styles/Jogostyle.css">
</svelte:head>

<script>

function Contagem(tabVazia,tabResposta) {
 let acertos = 0
 let erros = 0
	
	for(let i=0; i < tabResposta.length; i++){
		for (let j=0; j < tabResposta[i].length; j++){
			
		if(tabVazia[i][j] === tabResposta[i][j]){
				 return acertos++
		}else if(tabVazia[i][j] !== tabResposta[i][j]){
				 return erros++
		}
	}
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
	[],
	[]
	]
let tabelaResposta = [
	["A", "W", "Y", "Z", "K", "X","X","X","X","X"],  
	["B", "X", "X", "X", "X", "X","X","X","X","X"],
	["C", "X", "X", "X", "X", "X","X","X","X","X"],
	["X", "X", "X", "X", "X", "X","X","X","X","X"],
	["X", "X", "X", "X", "X", "X","X","X","X","X"],
	["X", "X", "X", "X", "X", "X","X","X","X","X"],
	["X", "X", "X", "X", "X", "X","X","X","X","X"],
	["X", "X", "X", "X", "X", "X","X","X","X","X"]
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
			{#each linha as tabelaResposta ,j}
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
